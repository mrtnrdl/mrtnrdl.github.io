---
layout: post
title:  "snapd on kali"
category: linux
author: mrtn
---

I've recently set up my old laptop (trusty old thinkpad t430s) again to use it as my daily downtime driver. as i do some bug hunting or testing out tools that might be handy during a pentest, i decided to go for a baremetal kali installation. i know, don't use kali as a daily driver, stick to a vm, etc etc. I promise you, i kinda know what i'm doing here ;) 

after completing the installation, i wanted to use `snapd`. So I just followed the [official documentation](https://snapcraft.io/docs/installing-snap-on-kali) and thought everything will work now. 

Turns out: It doesn't. 

First thing I realized was, that I didn't have `vs code` in my launcher and `/snap` wasn't part of my `$PATH`. The second part was easily fixed with a `export $PATH:/snap` in my `.zshrc`. For the launcher-problem, I needed some googling - but I found the solution quickly on [reddit](https://www.reddit.com/r/Kalilinux/comments/kn818t/snaps_not_visible_in_launcher/). Literally a missing link. 

```bash
ln -s /etc/profile.d/apps-bin-path.sh /etc/X11/Xsession.d/99snap 
```

After linking it and rebooting, `vs code` showed up in the launcher. Great - but now it still didn't start. 

Clicking the icon - nothing. 

Trying to launch `code` from the command line, an error got presented: `snap-confine has elevated permissions and is not confined but should be. Refusing to continue to avoid permission escalation attacks`. 

Turns out, there was a missing configuration for `apparmor`. After reading [this issue](https://github.com/canonical/microk8s/issues/249) on github, I pieced together a snippet to fix it: 


```bash
sudo apt install apparmor-utils apparmor-profiles && \
sudo apparmor_parser -r /etc/apparmor.d/*snap-confine* && \
sudo apparmor_parser -r /var/lib/snapd/apparmor/profiles/snap-confine* && \
sudo systemctl enable --now apparmor.service && \ 
sudo systemctl enable --now snapd.apparmor.service
```

After running this, even snaps that have to be installed with the `--classic` flag work again. 



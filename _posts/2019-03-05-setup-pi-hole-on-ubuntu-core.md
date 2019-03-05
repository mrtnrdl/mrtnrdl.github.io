---
layout: post
title:  "setup pi-hole on ubuntu core"
category: linux
author: mrtn
---

## goal

The internet gets more and more tracky, annoying and slower every day. After hearing from several people lately, that have tremendous fun with their pi-holes and the ability to surf the web without ads and trackers - even on devices that usually don't have adblockers, i decided to give it a go. 

## problem

The snap is not in the [snap store](https://snapcraft.io) (yet), but available via [github](https://github.com/pi-hole/docker-pi-hole). 
So yeah, `curl` - nope. Not available.
`wget`? nope. 
`nc` would be possible - but i'm not that keen on writing my get request just to download a zip-file from github... So the search began.

## solution 

After searching the net for quite some time, i've found out how to `git` on ubuntu core. This would enable me to clone the `snap` repository from github and install the pi-hole snap. 

Thanks to stackoverflow user [dehli](https://raspberrypi.stackexchange.com/users/31350/dehli), i mangaged to install `git` via the classic mode - where `apt` is still available. The following snippet is from his [answer](https://raspberrypi.stackexchange.com/questions/34120/how-to-install-git-in-pi-snappy) on stackoverflow. 

```
snap install classic --edge --devmode
sudo classic
sudo apt update
sudo apt install git
```

The rest should be working as described in the [readme](https://github.com/mrtnrdl/pihole-snap/blob/master/README.md). 

## alternative

If you do not want to add `git` to your system, you could also use `docker` and let the pi-hole run as a [docker application](https://github.com/pi-hole/docker-pi-hole). 


## closing thoughts

Now all you have to do is choose wisely. I have the feeling, that the docker-repository is way more active and therefore i tend to go with that way. On the other hand, i like the auto-updating feature of `snapd` pretty much and would like to use the snap. I'll definately will be watching the development of this! 

## tl;dr

to setup pi-hole on ubuntu core, either use `docker` or install `git` via the `classic` snap to add `git` to your system.

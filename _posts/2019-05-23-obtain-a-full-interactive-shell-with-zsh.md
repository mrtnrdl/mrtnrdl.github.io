---
layout: post
title:  "obtaining a full interactive shell with zsh"
category: infosec
author: mrtn
---

If I'll ever forget it again, hopefully i'll remember this post. 

After getting a connection on your reverse shell, we do not have a fully interactive shell yet. This is especially obvious if you try to `sudo` or something that requires a _real_ terminal. We are confronted with the problem, that `No TTY or askpass program is present`. 
To solve that, we can *upgrade* our shell. 

First, put your `netcat` session in the background with `ctrl + z`. 

Get the number of rows and columns with `stty -a | head -n1 | cut -d ';' -f 2-3 | cut -b2- | sed 's/; /\n/'`

To ignore hotkeys in the local shell and return to your reverse shell, enter `stty raw -echo; fg`. For *zsh users it is important to enter this in one line*.

Configure your rows and columns `stty rows ROWS cols COLS`

And now `export TERM=xterm-256color`

All you need to do now, is reload your shell: `exec /bin/bash`

Easier (if possible) is the classic python oneline `python -c 'import pty;pty.spawn("/bin/bash");'`



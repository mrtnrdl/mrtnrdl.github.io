---
layout: post
title:  "switching from gnu-screen to tmux"
category: linux
author: mrtn
---

After using linux (or any sort of unix-like operating system) for a few years, most users get pretty comfortable on the command line - and from time to time open several terminal windows/sessions just to avoid having to stare on the output of another long running process. If you find yourself in this position more often, you'll find yourself searching for a thing called [terminal multiplexers](https://en.wikipedia.org/wiki/Terminal_multiplexer). This is a tool that enables you to switch between multiple terminal-panes inside of your shell-session. Awesome, right? They also might offer you features like tiling vertical or horizontal, if you need to see several things at once. 

A few years back, I started using `gnu-screen` as my multiplexer. Recently I got a bit annoyed with it though. One thing that bothered me from the beginning was, that the name `screen` makes it pretty hard to find relevant information via online search engines. So it was almost always way more tedious to find the information i wanted as i would expect it... Something I also disliked more and more was, that I always had to open the same few panes after a while. I usually have very similar workloads and got used to having panes labeled as _nmap_, _gobust_ or _revshell_ (for example). 
And then I discovered `tmux-continuum` while reading [this post on stackoverflow](https://superuser.com/questions/440015/restore-tmux-session-after-reboot) - yes. `tmux`. Not screen - and the urge to finally ditch `gnu-screen` got strong enough. After reading several guides to switching, I decided that the work involved is not too much and that I would manage to do that within lunch break. And I went for it. 

See the `.tmux.conf` I currently use below: 

```bash
# set prefix to ctrl+a
unbind C-b
set -g prefix C-a

# toggling windows with ctrl+a ctrl+a
bind-key C-a last-window

# jump to the beginning of the line
bind a send-prefix

# don't rename windows automatically
set-option -g allow-rename off

# start with window number 1
set -g base-index 1

# Notifying if other windows has activities
setw -g monitor-activity on

# split panes using | and -
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

# vim copy mode
bind P paste-buffer
bind-key -T copy-mode-vi v send-keys -X begin-selection
bind-key -T copy-mode-vi y send-keys -X copy-selection
bind-key -T copy-mode-vi r send-keys -X rectangle-toggle
bind -t vi-copy y copy-pipe "xclip -sel clip -i"

# statusbar
set -g status-position bottom
set -g status-justify left

# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
set -g @plugin 'tmux-plugins/tmux-yank'

# tmux-continuum
set -g @continuum-restore 'on'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run -b '~/.tmux/plugins/tpm/tpm'
```

This offers me (so far) everything i need. From `vim`-like copy and pasting to preserving my opened panes, the status-line and the shortcuts that are deeply ingrained in my muscle-memory. 



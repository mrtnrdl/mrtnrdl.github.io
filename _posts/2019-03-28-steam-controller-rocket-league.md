---
layout: post
title:  "steam controller - the struggle with rocket league"
category: linux
author: mrtn
---

last week, i finally decided it's time for a controller again. as i have a somewhat spare older gaming pc here, i decided it's time to repurpose it. there is space behind the tv - why not using it as a steam box? 

while researching what controller to use - or if i should just buy wireless keyboard/mouse, i realized that the mainboard does not have bluetooth - so i need a dongle anyway. the steam controller comes _with_ a dongle already. well, why not, i thought? 

so i ordered it. it arrived reasonably fast (2 working days) and included batteries!

plug it in, updating firmware. 

with the right thumb-pad, you can controll the mouse. nice, the controller is usable for casual web-browsing! and obviously it got recognized by the os already. 

start steam in big picture mode - and the first weird thing happened. the controller settings said _no controller_ - after a minute of frantic web-searching, i realized i need to install the `steam-devices` package. did that, controller showed up. now let's start rocket league! the game for which i purchased the thing in the first place. 

controller works in the menu. 

join game

nothing. 

after hours and hours of web searching, messing with the config, restarting steam, recalibration etc, i found the following:

```
Forcing Steam Play/Proton because the Linux build has a bug with the Steam Controller support where the controller will not work in-game. 
Menus work fine, and changing to generic xinput controls work fine, 
but I want to use the native SIAPI support which works fine on the Windows build of the game. 
Steam Controller works perfectly with Rocket League using Steam Play/Proton.
```
[source](https://www.protondb.com/app/252950)

did that, enabled proton - and it *WORKS*. Thanks a lot, unknown proton user - i was starting to get really mad. I really hope this get's fixed soon, because it seems to be a pretty weird bug... Plus i now have to run `proton` wrapper for a game, that is natively supported. 

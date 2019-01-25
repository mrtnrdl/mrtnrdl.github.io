---
layout: post
title:  "the infosec mindset"
category: infosec
author: mrtn
---

after being interested in hacking, malware, intrusion detection, social engineering and all the funny and interesting things that define the _infosec_ field, i decided to drink from the fountain. i took the plunge and decided to invest in it and finally got serious with it. i started learning more, reading more and took part in ctfs. 

after solving a few of the easy machines on [hackthebox](https://www.hackthebox.eu), i started to realize something:
- you always learn
- you're forever a noob
- sharing is caring. i got so much help and support that it would feel weird not to "give back" in some way
- security is a mindset

the thing is the most important, and i'd like to elaborate a bit more on that. why should security be a mindset? isn't it something that is easily solved with technology? in the end, it's the technology that gets exploited, aye? 

well, yes and no. there are lots of exploit out there that use weaknesses in the code. but yet, one of the most important - if not *the most important* attack vector is the human sitting in front of the keyboard. ask every experienced social engineer (or most children) - humans want to help and they want to make your life easier. 
so being aware of the human nature is one part of a security-aware mind. being aware, that someone might want to exploit _you_. not the computer in front of you, not the smartphone on your table. you are the target. because sometimes it's just easier asking for a password than exploiting a vulnerability. 

another part of the security mindset affects the developer. the developer (as a persona) is very target-oriented. they want to _get stuff done_, implement yet another feature and are very methodical. tests get written, documentation gets writte - and before that user stories are breaken down into tasks and the necessary information gets extracted. 
all of this is part of the process, that defines the image, that the programmer has in their mind. an image, that is filled with _what needs to work_ - and sometimes with the _how_. maybe they also have some test cases in mind. this can be pretty dangerous, because the developers might focus only on the expected behaviour, expected input etc. but what with all the edge cases? speaking from personal experience, this happens quite a lot. the owasp top-10 do not by accident contain lots of easily mitigated stuff. dealing with sql injections is really not a technical problem in 2019... 

but even with security-conscious developers, this is not yet solved. the best team of security-aware developers can be mislead by or severly limited in their abilities by a product owner (or whoever creates the user-stories/specification) that focusses on features and on features alone. especially when time or budget is short (and it kinda always is), then security can easily be ignored ("if we don't look, everything is secure, right?") or be seen as a competitive disadvantage. creating a secure product is hard and expensive. at least more expensive than just ignoring security completely. as long as the customers don't take their money somewhere else to punish organisations that obviously don't care about their security, nothing will change in that regard.

and with customers in mind, we reached the next group where a security mindset could pay off: the paying customers. if scandals, breaches and gaping security holes are not enough to turn your back on some companies and products - well, why should anything change? if we do not vote with our money, nothing will change and everbodies data will be public in the end. 

*tl;dr*
security is a mindset. developers, product-owners and customers can profit from developing an eye for security in the products they use - or we will be faced with more and more breaches.  

---
layout: post
title:  "first visit @aws meetup nuremberg"
category: personal
author: mrtn
---

after subscribing to the [meetup](https://www.meetup.com/de-DE/Nurnberg-AWS-User-Group/) itself a while ago, today is the first occasion i made it to the aws meetup in nuremberg. the topic that caught my attention and made me leave my cozy home was _Zero Trust in AWS_. Eduardo [Rocha](https://www.globaldots.com/about-us/our-team/), Senior Sales Engineer and Security Analyst at GlobalDots, will give an overview about the implementation of zero trust concepts on Amazon Web Services. 

Eduardo started out with explaing the _Zero Trust_ concept in general. The perimeter is dead, because the way we work changed (fuck yeah!) - people tend not to drive in the same office building every day. They are travelling between customers, working on the go or simply stay at home where they work. In addition to that, there has been a change in how companies do _IT_. Instead of maintaining a huge and costly datacenter, they started using the solutions cloud providers like aws offer. Scale on demand and use hosted services instead of maintaining everything by themselves. 
 To re-create something that is similar to the oldschool perimeter of the past would have two effects:
- it's expensive, because you'd need more infrastructure
- you would miss out on a lot of the flexibility of _the cloud_

So he explained, that it makes sense to operate under the assumption that you are navigating in hostile waters. to mitigate this and as one key element, he identified exhaustive logging and verifying.

so the proposed solution, that his company is dog-fooding already: adopting a _cloud perimeter_
- leverage a zero trust security and delivery model for successful digital transformation
- data plane/control plane
- log everything
- verify everything

Unfortunately, we got stuck discussing performance issues, scalability and wether or not this is something _new_ instead of focussing on the concept in general - i would have been really interested, how they implemented trust in that system. are things like geolocation, time of the day, device-id's etc taken into consideration, when the controller decides if you can access the services?


Afterwards there was another talk about siemens mindsphere and there was pizza - unfortunately i had to leave a bit early, because it was already getting late. 

Although i was a bit disappointed of the technical depth and the way the discussion took, i'll be definately be back at the aws meetup. and it got me curious, what direction and implementations of zero trust techniques we will see over the course of the next few years.

 

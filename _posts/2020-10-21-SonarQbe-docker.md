---
layout: post
title:  "Start your SonarQube Server in a local docker container"
category: linux
author: mrtn
---

As I always have to search for that - I'll take the liberty of saving me the hassle of googling it all the time. 


```
docker pull sonarqube
docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest
```

Then: Go to http://localhost:9000 and log in with `admin:admin`

That's it. 

 

---
layout: post
title:  "clone a webpage with .git exposed"
category: infosec
author: mrtn
---

If you ever have discovered an exposed `.git` folder on a webpage and asked yourself *how do i clone the damn thing?*

```bash
wget --mirror -I .git http://TARGET.com/.git/
```

Then you can just use

```bash
git checkout -- . 
```

to reset the branch and use `git` as you are used to - discover secrets and/or flaws. 


**hack the planet** or at least the web \m/

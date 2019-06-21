---
layout: post
title:  "`find` on windows"
category: infosec
author: mrtn
---

If you find yourself on a _Windows_ host and desperately search for a file, remember 

```bash
dir \s\b\a <filename>
```

This commands acts as an 'as good as it gets' replacement for the classic unix `find` command. 


*s* includes all sub-folders

*b* bare format (no heading, file size, summary)

*a* display all files




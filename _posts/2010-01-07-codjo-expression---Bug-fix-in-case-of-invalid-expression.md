---
layout: post
title: agf-expression - Bug fix in case of invalid expression
tags: [framework-1-129,codjo-expression]
---
<u>Context</u>:
During an Oscar segmentation task, a severe failure occured which made impossible to successfuly launch new workflow tasks.
This was due to a not catched ```Error``` in ```codjo-expression```.

<u>Description</u>:
Now, the ```Error``` is correctly catched.
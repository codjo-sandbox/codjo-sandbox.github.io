---
layout: post
title: agf-segmentation - Bug fix in case of invalid formula
tags: [framework-1-129,codjo-segmentation]
---
<u>Context</u>:
During an Oscar segmentation task, a severe failure occurred which made impossible to successfully launch new workflow tasks.

<u>Description</u>:
```codjo-segmentation``` has been modified in order to inform the ```SegmentationJobAgent``` of failures which occurred.

see: [[framework:/2010/01/07/codjo-expression - Bug fix in case of invalid expression], [framework:Documentation agf-segmentation]]
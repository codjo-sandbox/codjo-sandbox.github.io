---
layout: post
title: agf-mad - Minor refactoring in AbstractAction
tags: [framework-1-123,codjo-mad]
---
<u>Context</u>

The ```displayNewWindow()``` method can be useful in derivative classes of ```AbstractAction```.

<u>Description</u>

Therefore, its access privilege was promoted to ```protected```.
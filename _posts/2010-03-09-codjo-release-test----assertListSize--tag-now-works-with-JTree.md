---
layout: post
title: agf-release-test - "assertListSize" tag now works with JTree
tags: [framework-1-137,codjo-release-test,hot-topics]
---
<u>Context</u>:
For ```damas``` release tests, we need to assert the number of rows displayed in a ```JTree```.

<u>Description</u>:
```assertListSize``` has been enhanced to work with ```JTree``` allowing to assert ```JTree``` **visible** row count.

<u>Example</u>:
```xml
<assertListSize name="ReferentialList" expected="1"/>
```

see: [[framework:codjo-release-test - Tags IHM#assertListSize]]
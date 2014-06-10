---
layout: post
title: agf-mad - Bug fix - NullPointerException when opening some RequestTable
tags: [framework-1-162,codjo-mad]
---
<u>Context</u>:
```NullPointerException``` occured (since codjo-mad 3.135) when opening ```RequestTable``` with preference using ```sorter``` with class name.

<u>Description</u>:
The problem has been corrected in ```MadComparator``` class.

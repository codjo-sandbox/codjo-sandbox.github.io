---
layout: post
title: agf-mad - StringMadComparator not case sensitive anymore
tags: [framework-2-5,codjo-mad]
---
<u>Context</u>
Implementation of string comparator was case sensitive.
Sort's result for ```"b","AL","Ac"``` was ```"AL","Ac","b"```.

<u>Description</u>
New implementation is not case sensitive.
Sort's result for ```"b","AL","Ac"``` is now ```"Ac","AL","b"```.

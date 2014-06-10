---
layout: post
title: agf-mad - Horizontal scrollbar policy constants replaced by enum
tags: [framework-1-138,codjo-mad]
---
<u>Context</u>:
In the previous version of the framework constants were introduced to specify the horizontal scrollbar policy : [[framework:/2010/03/03/codjo-mad - Horizontal scrollbar policy]].
It was not reliable to have too many constants in the class.

<u>Description</u>:
Constants have been replaced by an enum.

<u>Example</u>:
```java
requestTable.setHorizontalScrollBarPolicy(ScrollBarPolicy.HORIZONTAL_SCROLLBAR_SHOW_IF_NEEDED);
```

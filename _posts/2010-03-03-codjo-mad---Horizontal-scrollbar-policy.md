---
layout: post
title: agf-mad - Horizontal scrollbar policy
tags: [framework-1-137,codjo-mad,hot-topics]
---
<u>Context</u>:
Working with a ```RequestTable``` with many columns, the table view wasn't efficient:
![Alt attribute text Here](attachments/noScrollBar.JPG)

<u>Description</u>:
```setHorizontalScrollBarPolicy(int```) has been created in ```RequestTable```.
This method allow users to make the horizontal scrollbar appearing when needed:
![Alt attribute text Here](attachments/withScrollBar.JPG)

<u>Example</u>:
```java
requestTable.setHorizontalScrollBarPolicy(RequestTable.HORIZONTAL_SCROLLBAR_SHOW_IF_NEEDED);
```

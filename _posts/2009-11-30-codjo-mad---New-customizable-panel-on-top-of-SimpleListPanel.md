---
layout: post
title: agf-mad - New customizable panel on top of SimpleListPanel
tags: [framework-1-124,codjo-mad]
---
<u>Context</u>:
It was needed to have custom component above the ```RequestTable``` in ```SimpleListGui```.

<u>Description</u>:
Two methods have been created:
```java
SimpleListGui.getHeaderPanel();

SimpleListPanel.getHeaderPanel();
```
They allow to access the panel above the ```RequestTable``` and do stuff like this:

![Alt attribute text Here](attachments/Snapshot.JPG)

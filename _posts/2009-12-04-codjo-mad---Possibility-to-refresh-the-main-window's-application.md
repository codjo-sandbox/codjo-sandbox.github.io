---
layout: post
title: agf-mad - Possibility to refresh the main window's application
tags: [framework-1-125,codjo-mad]
---
<u>Context</u>
AAAm users need sometimes to launch their application in the REC/PROD environment at the same time. They'd like to have visual effect to differentiate them.

<u>Description</u>
We customize the look and feel for the main window. 
To do this, we need to add a method in ```MadGuiCore``` which simply refreshes the UI of the main window:
```java
    public void updateMainWindowTreeUI()
```

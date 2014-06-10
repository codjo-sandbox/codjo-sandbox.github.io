---
layout: post
title: agf-mad - The record count component in the toolbar can be changed
tags: [framework-1-118,codjo-mad]
---
The ```RequestToolBar``` displays on its left a ```RequestRecordCountField``` which could not be accessed from the outside.

A modification in the ```RequestToolBar``` allows an application to modify or replace that component:
```title=RequestToolBar.java
public java.awt.Component getLeftComponent()

public void setLeftComponent(java.awt.Component)
```

This new API is used for [[quarantine windows|http://wp-confluence/confluence/x/ZIDO]].

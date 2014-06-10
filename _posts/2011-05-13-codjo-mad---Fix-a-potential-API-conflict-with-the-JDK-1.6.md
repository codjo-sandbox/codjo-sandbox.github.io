---
layout: post
title: agf-mad - Fix a potential API conflict with the JDK 1.6
tags: [framework-1-198,codjo-mad,jdk16-migration]
---
<u>Context</u> 
During the JDK 6 migration impact study, we discovered that the method ```RequestTable.convertRowIndexToModel(int)``` is in conflict with the API change introduced by the JDK 1.6 (silent override).

see: [[jdk16-migration]]

<u>Description</u> 
The method ```convertRowIndexToModel(int)``` of the ```RequestTable``` has been renamed into ```convertRowIndexToModelIndex(int)```.


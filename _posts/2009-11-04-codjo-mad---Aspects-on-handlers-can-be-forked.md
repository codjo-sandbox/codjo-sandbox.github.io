---
layout: post
title: agf-mad - Aspects on handlers can be forked
tags: [parallel-workflow,framework-1-120,codjo-mad]
---
<u>Context</u>:
This task is part of a more global project _"Audit improvement of server tasks"_. 

see: architecture meetings ([[1|swdev:Reunion architecture du 20090918 - Audit Workflow] / [2|swdev:Reunion architecture du 20090925 - Audit Workflow - IHM] / [3|swdev:Reunion architecture du 20090929 - Audit Workflow - mad, aspect, planification]])
see: [[/2009/11/04/codjo-aspect - Fork mode added on join points]]
see: [[/2009/11/04/codjo-workflow - Implementation of the aspect fork mode for agf-mad]]

<u>Description</u>:
By now, aspects defined on ```codjo-mad``` handlers may be executed in "fork" mode (using an ```agf-workflow``` agent). Fork mode is only available on "after" join points. 

<u>Example</u>: 
```
<join-point call="after" point="handler.execute" argument="selectAllStuff" isFork="true"/>
```

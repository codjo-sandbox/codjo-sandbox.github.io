---
layout: post
title: agf-pom - Upgrade of mockito
tags: [framework-2-18,codjo-pom,hot-topics,codjo-imports,codjo-sql,codjo-referential,codjo-administration,codjo-segmentation,codjo-tokio,codjo-control,codjo-mad]
---
<u>Context</u>:
Need the use of ```Mockito.doCallRealMethod``` (start to be present in version 1.8 of ```mockito```).

<u>Description</u>:
The version has been upgraded to the last version: ```1.9.0```.
This implies the replacement in ```DepedencyTest``` tests of: 
```
-> org.mockito.internal.progress
```
by:
```
-> org.mockito.stubbing
```
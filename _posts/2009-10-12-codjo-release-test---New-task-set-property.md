---
layout: post
title: agf-release-test - New task set-property
tags: [framework-1-117,codjo-release-test,hot-topics]
---
**Defines the value of a property depending on the execution mode (remote/local) of the test release**

This task allows to define a property, with two different values,
whether the test release is executed remotely or locally.
```xml
<set-property name="my.property"  remoteValue="remoteval" localValue="localval" />
```
In the remote mode, ```my.property``` will have the value ```remoteval```.
In the local mode, ```my.property``` will have the value ```localval```.

**The properties are expanded correctly :**
When prefix has value ```"/usr/bin"```
```xml
<set-property name="my.property"  remoteValue="${prefix}/remoteval" localValue="${prefix}/localval" />
```
In the remote mode, ```my.property``` will have the value ```/usr/bin/remoteval```.
In the local mode, ```my.property``` will have the value ```/usr/bin/localval```.
\\

cf. tag documentation : [[set-property]]
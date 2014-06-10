---
layout: post
title: agf-workflow - Permettre le lancement en mode asynchrone
tags: [codjo-workflow,framework-1-13]
---
Il est maintenant possible de déclancher via ```ScheduleLauncher``` un workflow en mode asynchrone. 

Pour cela il suffit de faire : 

```java
ScheduleLauncher launcher = new ScheduleLauncher(myId);
launcher.setExecuteType(ScheduleLauncher.ExecuteType.ASYNCHRONOUS);
launcher.executeWorkflow(...);
```

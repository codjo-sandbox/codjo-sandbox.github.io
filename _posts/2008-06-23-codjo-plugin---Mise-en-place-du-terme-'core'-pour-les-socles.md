---
layout: post
title: agf-plugin - Mise en place du terme 'core' pour les socles
tags: [codjo-plugin,framework-1-49,hot-topics]
---
Le terme 'core' est utilisé pour identifier rapidement les socles mis à disposition par le framework.

Les classes suivantes ont été renommées, mais l'ancienne classe est gardée pour compatibilité ascendante: 
* ```ApplicationPluginManager``` -> ```ApplicationCore```
* ```BatchClient``` -> ```BatchCore```
* ```AgentServer``` -> ```ServerCore```
* ```AgentNode``` -> ```NodeCore```

Les classes suivantes ont été renommées en supprimant l'ancienne classe : 
* ```ApplicationPluginManagerTestCase``` -> ```ApplicationCoreTestCase```
* ```ApplicationPluginManagerMock``` -> ```ApplicationCoreMock```

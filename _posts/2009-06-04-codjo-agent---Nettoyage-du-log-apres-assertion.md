---
layout: post
title: agf-agent - Nettoyage du log après assertion
tags: [framework-1-97,codjo-agent]
---
La méthode ```logAndClear``` a été ajoutée dans ```AgentAssert```. Elle permet de vérifier le contenu d'un ```LogString``` puis de le nettoyer si l'assertion est vérifiée.

Exemple :
```java
story.record()
        .addAssert(AgentAssert.logAndClear(log, "start()"));

story.record()
        .(...)

story.record()
        .addAssert(AgentAssert.logAndClear(log, "stop()"));
```
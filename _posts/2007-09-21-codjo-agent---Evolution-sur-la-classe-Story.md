---
layout: post
title: agf-agent - Evolution sur la classe Story
tags: [codjo-agent,framework-1-13]
---
Ajout de la méthode utilitaire ```installService``` permettant d'installer des services JADE pour l'execution de test.

Exemple d'utilisation : 
```java
// Le service MySecurityService sera accessible par l'agent "notifier-agent"
story.installService(MySecurityService.class);

story.record().startAgent("notifier-agent", createNotificationAgent());
...
story.execute();
```

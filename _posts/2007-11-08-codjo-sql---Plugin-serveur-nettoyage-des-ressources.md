---
layout: post
title: agf-sql - Plugin serveur nettoyage des ressources
tags: [framework-1-19,codjo-sql]
---
Le plugin ```JdbcServerPlugin``` libère maintenant correctement les ressources prises lors du ```start```.

```java
 public void stop() {
  pluginManager.removeGlobalComponent(JdbcManager.class);
  ...
 }
```

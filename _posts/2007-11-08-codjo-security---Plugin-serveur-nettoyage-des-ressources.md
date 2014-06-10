---
layout: post
title: agf-security - Plugin serveur nettoyage des ressources
tags: [framework-1-19,codjo-security]
---
Le plugin ```SecurityServerPlugin``` libère maintenant correctement les ressources prises lors du ```start```.

```java
public void stop() {
  container.removeGlobalComponent(SecurityContextFactory.class);
  container.removeGlobalComponent(UserFactory.class);
  container.removeGlobalComponent(ServerModelManager.class);
}
```



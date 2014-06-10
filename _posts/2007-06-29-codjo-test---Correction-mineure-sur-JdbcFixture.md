---
layout: post
title: agf-test - Correction mineure sur JdbcFixture
tags: [codjo-test,framework-1-4]
---
Amélioration du retour d'erreur lors de l'utilisation de ```JdbcFixture```.

Lors de l'appel 

```java
jdbc = JdbcFixture.newTokioFixture();
```

Si le fichier ```tokio.properties``` est introuvable l'erreur suivante est remontée : ```Fichier '/tokio.properties' introuvable```

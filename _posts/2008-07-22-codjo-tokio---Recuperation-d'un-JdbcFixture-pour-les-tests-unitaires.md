---
layout: post
title: agf-tokio - Récupération d'un JdbcFixture pour les tests unitaires
tags: [framework-1-53,codjo-tokio,hot-topics]
---
Précédemment, pour récupérer un ```JdbcFixture``` pour les tests applicatifs, il fallait utiliser la méthode ```JdbcFixture.newTokioFixture()``` de ```codjo-test```.
Maintenant, il faut passer par la classe ```Tokio``` de ```codjo-tokio```.

<u>Exemple</u> :
```java
JdbcFixture jdbcFixture = Tokio.newJdbcFixture();
```
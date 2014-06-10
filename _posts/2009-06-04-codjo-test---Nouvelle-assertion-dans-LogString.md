---
layout: post
title: agf-test - Nouvelle assertion dans LogString
tags: [framework-1-99,codjo-test]
---
La classe ```LogString``` s'enrichit d'une nouvelle méthode : ```assertAndClear(String)```.
Cette méthode permet de vider le ```LogString``` après avoir vérifié qu'il contenait la valeur attendue.

<u>Exemple</u>
```java
LogString log = ...;
log.call("doIt");
log.assertAndClear("doIt");
log.assertContent(""); // Le LogString a été vidé
```
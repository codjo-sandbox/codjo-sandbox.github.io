---
layout: post
title: agf-tokio - Récupération de table par son nom est indépendante de la casse
tags: [framework-1-62,codjo-tokio]
---
La méthode ```DataSet.getTable(string)``` utilisée, dans l'API tokio, pour récupérer une table est maintenant indépendante de la casse.

<u>Exemple</u> : 
```java
assertEquals("TableA", scenario.getInputTable("tablea").getName());
```
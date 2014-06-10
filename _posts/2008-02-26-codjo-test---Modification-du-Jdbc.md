---
layout: post
title: agf-test - Modification du Jdbc
tags: [codjo-test,framework-1-33]
---
Ajout d'une méthode utilitaire permettant l'affichage du résultat d'une requête SQL. Cette méthode est notamment pratique pour afficher le contenu d'une requête avec jointure. 

<u>Exemple</u> : 
```java
JdbcFixture jdbc = ....
jdbc.spoolQuery("select * from AP_TABLE", System.out);
```

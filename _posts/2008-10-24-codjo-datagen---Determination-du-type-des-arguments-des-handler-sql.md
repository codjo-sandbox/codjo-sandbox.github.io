---
layout: post
title: agf-datagen - Détermination du type des arguments des handler-sql
tags: [framework-1-67,codjo-datagen]
---
[[codjo-datagen]] permet de déterminer le type de certains arguments des ```handler-sql``` en fonction de la définition de l'```entity```.
Jusqu'alors, cette détermination ne prenait en compte que les ```properties``` définies directement au niveau de l'```entity```.

Maintenant, les ```properties``` sont aussi déterminées à partir des ```structures``` rattachées à l'```entity``` (```audit``` par exemple).

Pour l'instant, seuls les types suivants sont traités de manière spécifique :
- ```java.sql.Date```
- ```java.sql.Timestamp```
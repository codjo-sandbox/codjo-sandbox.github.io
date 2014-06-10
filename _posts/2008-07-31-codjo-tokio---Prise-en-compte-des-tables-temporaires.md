---
layout: post
title: agf-tokio - Prise en compte des tables temporaires
tags: [framework-1-55,codjo-tokio]
---
La description des tables dans les fichiers ```tokio``` a évolué afin de pouvoir spécifier si une table est temporaire ou non.
Par défaut, une table est considérée comme non temporaire.

```xml
<table name="MA_TABLE" temporary="true">
   ...
</table>
```

Cette modification permet de gérer correctement les tables temporaires indépendamment du type de la base, les tables temporaires n'étant pas toujours gérées de la même manière. 
Par exemple, en Sybase le fait de spécifier temporary à vrai rajoute le caractère # en début de nom de table.

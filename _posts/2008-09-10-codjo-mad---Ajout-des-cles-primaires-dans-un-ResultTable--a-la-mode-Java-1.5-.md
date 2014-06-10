---
layout: post
title: agf-mad - Ajout des clés primaires dans un ResultTable "à la mode Java 1.5"
tags: [framework-1-61,codjo-mad]
---
Ajout de la méthode ```setPrimaryKeys``` dans la classe ```ResultTable``` en lui passant une série de chaînes de caractères :

```
public void setPrimayKeys(String... keys);
```

Par exemple :
```
resultTable.setPrimaryKeys("Fred", "Paulo");
```


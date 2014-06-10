---
layout: post
title: agf-mad - Mise à jour du StructureReader pour prendre en compte l'attribut sql-primary-key
tags: [framework-1-69,codjo-mad]
---
La structure ```FieldStructure``` comprend maintenant une nouvelle méthode ```isSqlPrimaryKey()```.

Exemple d'utilisation :
```
DetailDataSource dataSource = ...;
boolean isPrimaryKey = dataSource.getStructureReader()
                                 .getTableByJavaName("maTable")
                                 .getFieldByJava("monChamp")
                                 .isSqlPrimaryKey();
```

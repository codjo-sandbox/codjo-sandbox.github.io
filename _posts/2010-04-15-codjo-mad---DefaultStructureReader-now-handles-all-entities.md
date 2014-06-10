---
layout: post
title: agf-mad - DefaultStructureReader now handles all entities
tags: [framework-1-143,codjo-mad]
---
<u>Context:</u>
see [[swdev:Reunion architecture du 20100415 - Probleme StructureReader incomplet si datagen contient plusieurs entites utilisant un même nom de table (suite et fin)]]

<u>Description:</u>
The class ```DefaultStructureReader``` contains two ```Map<String, TableStructure>```:

* one with the java name as key (this map is used by the method ```containsTableByJavaName```, ```getAllTableStructure```, ```getTableByJavaName```)

* one with the sql name as key (this map is used by the method ```containsTableBySqlName```, ```getTableBySqlName```)

The method ```getAllTableStructure``` now return a ```Collection``` of ```TableStructure```.

 
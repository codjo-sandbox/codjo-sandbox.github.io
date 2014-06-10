---
layout: post
title: agf-mad - Add attribute FunctionalKey on FieldStructure
tags: [framework-1-172,codjo-mad]
---
<u>Context</u>:
On Mint application, we need to know if a field belongs to the functional key of the entity.

<u>Description</u>:
The method ```isFunctionalKey``` is added to the interface ```FieldStructure```.
The method ```getFunctionalKeyFields``` which return a list of field names, is added to the interface ```TableStructure```.

To stay consistent a similar method ```getSqlPrimaryKeyFields``` is also added on ```TableStructure```.

This modification is related to [[framework:/2010/10/25/codjo-datagen - Add functional key information in structure.xml file]]
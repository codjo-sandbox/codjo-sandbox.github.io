---
layout: post
title: agf-mad - Prise en compte des champs obligatoires par le DetailDataSource
tags: [codjo-mad,framework-1-93,hot-topics]
---
Lors de la déclaration des champs sur le ```DetailDataSource```, ce dernier identifie si ces champs sont requis en se basant sur la définition des champs faite au niveau des fichiers datagen.

Une méthode publique sur le ```DetailDataSource``` permet de savoir si un champ donné est requis :
```
public boolean isFieldRequired(String fieldName)
```
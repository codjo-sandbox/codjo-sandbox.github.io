---
layout: post
title: agf-confluence - Ajout de méthodes de suppression de label
tags: [framework-1-73,codjo-confluence]
---
L'interface ```ConfluenceOperations``` a été enrichie des méthodes suivantes :
```
public void removeLabelByName(String objectId, String labelName) throws ConfluenceException...

public void removeLabelByName(String labelName) throws ConfluenceException...
```
La première méthode permet de supprimer un label dans une page précise, tandis que la deuxième méthode supprime ce label de toutes les pages.
---
layout: post
title: agf-mad - Ajout méthode hasBeenUpdated(String... fieldNames)
tags: [codjo-mad,framework-1-46]
---
Cette méthode permet de savoir si un ou plusieurs champs d'une ```DetailDataSource``` ont été modifiés.

Exemple d'utilisation :

```
// true si le champ isinCode à été modifié
boolean updated = detailDataSource.hasBeenUpdated("isinCode");

// true si le champs isinCode ou rate ont été modifiés
boolean updated = detailDataSource.hasBeenUpdated("isinCode", "rate"); 
```
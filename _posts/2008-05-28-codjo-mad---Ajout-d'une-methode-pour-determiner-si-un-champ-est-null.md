---
layout: post
title: agf-mad - Ajout d'une méthode pour déterminer si un champ est null
tags: [codjo-mad,framework-1-46]
---
Ajout dans la classe ```DetailDataSource``` de la méthode : 

```public boolean isFieldNull(String fieldName);```

Exemple d'utilisation :

```
// true si isinCode est null
boolean isNull = detailDataSource.isFieldNull("isinCode"); 
```
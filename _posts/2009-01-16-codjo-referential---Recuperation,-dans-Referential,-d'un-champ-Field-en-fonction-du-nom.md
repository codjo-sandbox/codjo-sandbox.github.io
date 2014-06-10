---
layout: post
title: agf-referential - Récupération, dans Referential, d'un champ Field en fonction du nom
tags: [framework-1-79,codjo-referential]
---
Ajout dans la classe ```Referential``` d'une méthode permettant de récupérer un champs ```Field``` en fonction du nom de celui-ci

```
    public Field getField(String fieldName) {
        return fieldList.get(fieldName);
    }
```
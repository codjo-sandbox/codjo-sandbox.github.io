---
layout: post
title: agf-agent - Ajout de la possibilité d'ajouter des propriétés aux ServiceDescriptions
tags: [codjo-agent,framework-1-54]
---
Il est maintenant possible de passer des propriétés aux ```ServiceDescription```. Exemple :
```
ServiceDescription service = new ServiceDescription();
service.addProperty("wsig", "true");
```
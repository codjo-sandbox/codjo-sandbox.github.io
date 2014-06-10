---
layout: post
title: agf-mad - Amélioration du retour d'erreur de la méthode "FieldsList.getFieldValue()"
tags: [framework-1-62,codjo-mad]
---
Amélioration du retour d'erreur de la méthode ```FieldsList.getFieldValue(fieldName)```. Dorénavant, la méthode renverra dans tous les cas limites une ```IllegalArgumentException``` lorsque le field n'est pas défini.


---
layout: post
title: agf-mad - Enrichissement des propriétés envoyées par ListDataSource
tags: [codjo-mad,framework-1-11]
---
ListDataSource envoie maintenant les évènements spécifiques suivants :
* ListDataSource.ADDED_ROW_PROPERTY sur un ajout de ligne,
* ListDataSource.REMOVED_ROW_PROPERTY sur une suppression de ligne,
* ListDataSource.UPDATED_ROW_PROPERTY sur une mise à jour de la ligne.
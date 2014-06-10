---
layout: post
title: agf-mad - Ajout d'une méthode pour ajouter ou modifier un champ dans une liste
tags: [framework-1-113,codjo-mad]
---
La méthode ```void addOrUpdateField(String, String)``` permet d'ajouter un champ avec une valeur, ou de modifier la valeur si le champ existait déjà dans l'objet ```FieldsList```.

Auparavant, il était systématiquement nécessaire de tester l'existance du champ pour appeler la méthode adéquate, sinon une exception de type ```IllegalArgumentException``` était lancée.
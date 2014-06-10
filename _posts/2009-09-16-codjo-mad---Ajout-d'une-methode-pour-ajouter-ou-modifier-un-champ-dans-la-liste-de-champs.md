---
layout: post
title: agf-mad - Ajout d'une méthode pour ajouter ou modifier un champ dans la liste de champs
tags: [codjo-mad,framework-1-113]
---
La méthode void addOrUpdateField(String, String) permet d'ajouter un champ avec une valeur, ou de modifier la valeur si le champ existait déjà dans l'objet FieldsList.

Auparavant, il était systématiquement nécessaire de tester l'existance du champ pour appeler la méthode adéquate, sinon une exception de type IllegalArgumentException (non déclarée dans la signature) était lancée.

 
 

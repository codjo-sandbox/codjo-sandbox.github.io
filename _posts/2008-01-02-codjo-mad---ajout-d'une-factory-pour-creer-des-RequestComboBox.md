---
layout: post
title: agf-mad - ajout d'une factory pour créer des RequestComboBox
tags: [framework-1-25,codjo-mad]
---
La classe RequestComboBoxFactory permet de creer et de charger une requestComboBox.

Actuellement une seule méthode possible : ```createRequestCombobox```
qui accepte 3 paramètres :
* handlerId : nom du handler qui permet de charger les données
* keyColName&nbsp;: Nom de la colonne affichée et stochée
* containsNull : Indique si la requestComboBox accepte ou non les valeurs nulles

Exemple:&nbsp;
```
RequestComboBoxFactory.createRequestCombobox("handlerID", "columnName", false);
```
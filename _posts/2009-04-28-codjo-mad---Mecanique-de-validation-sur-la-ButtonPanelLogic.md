---
layout: post
title: agf-mad - Mécanique de validation sur la ButtonPanelLogic
tags: [codjo-mad,framework-1-93]
---
Une mécanique de validation a été ajoutée sur la ```ButtonPanelLogic```. Elle permet de spécifier un objet chargé de valider les données des ```DataSource``` qui lui sont associés.

Une méthode publique permet de spécifier un "validateur" :
```
public void setButtonLogicValidator(ButtonLogicValidator buttonLogicValidator)
```

Le validateur spécifique, ```RequiredFieldsValidator``` a été implémenté pour pouvoir gérer les champs requis.
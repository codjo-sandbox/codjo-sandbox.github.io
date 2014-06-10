---
layout: post
title: agf-gui-toolkit - Enrichissement de la saisie du NumberField
tags: [codjo-gui-toolkit,framework-1-30]
---
Ajout d'un nouveau champ ```validInputNumberExpression``` qui correspond à une expression regulière et empeche toute saisie non conforme.

Ex: Cet implémentation empeche la saisie de plus de six décimales pour les nombres positifs/négatifs.

```
NumberField myNumberField = new NumberField();
myNumberField.setValidInputNumberExpression("-?\\d*.?\\d{0,6}");
```
---
layout: post
title: agf-gui-toolkit - Ajout d'un construteur dans NumberFieldEditor
tags: [framework-1-82,codjo-gui-toolkit]
---
Le constructeur suivant a été ajouté dans cette classe :
```
public NumberFieldEditor(int maxDigit, int maxFractionDigit, boolean canBeNegative)
```
Ce constructeur permet d'autoriser la saisie de nombre négatifs dans la même limite en valeur absolue qu'en positif (paramétrée avec ```maxDigit``` et ```maxFractionDigit```)

Exemple:

```
NumberFieldEditor(8, 2, true);
```

Le nombre qui pourra être saisi est compris entre -999 999.00 et 999 999.00
---
layout: post
title: agf-gui-toolkit - Correction de la couleur du NumberField
tags: [framework-1-100,codjo-gui-toolkit]
---
Le NumberField peut arriver à un état où toute saisie apparaît comme erronée (c'est-à-dire en rouge).

Il faut pour cela suivre une certaine séquence d'actions. Par exemple :
1. Dans&nbsp;un NumberField limité à 3 chiffres, entrer 1234 (qui apparaît en rouge)
1. Appuyer sur un bouton qui charge une valeur&nbsp;valide dans&nbsp;le NumberField
1. Entrer un nombre valide : il apparaît alors en rouge.

&nbsp;Ce bug a été corrigé.
---
layout: post
title: agf-datagen - Possibilité de gérer les clés étrangères dans les référentiels
tags: [framework-1-8,codjo-datagen]
---
Mint possède un référentiel dont 1 champ dépend d'un autre référentiel. Si Datagen détecte la présence de clés étrangères alors il génèrera le handler correspondant à la colonne concernée. Ainsi pour la gestion des référentiels génériques (**codjo-referential**), sur le détail d'un enregistrement d'un référentiel ayant cette particularité, une combobox sera générée.
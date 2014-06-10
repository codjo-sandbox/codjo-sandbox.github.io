---
layout: post
title: agf-datagen - Optimisation de la génération
tags: [framework-1-102,codjo-datagen]
---
Pour la génération, ```datagen``` construit un fichier intermédiaire ```final.xml```.
Précédemment, ce fichier était systématiquement produit même si la génération n'était pas nécessaire.
Maintenant, ce fichier n'est produit que s'il y a eu des modifications.

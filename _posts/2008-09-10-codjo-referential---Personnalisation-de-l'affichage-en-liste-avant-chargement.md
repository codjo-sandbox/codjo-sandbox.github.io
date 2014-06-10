---
layout: post
title: agf-referential - Personnalisation de l'affichage en liste avant chargement
tags: [framework-1-60,codjo-referential]
---
La méthode ```handleListOpen``` du ```ListGuiCustomizer``` est, de nouveau, appelée avant le chargement de l'affichage en liste. Cela permet notamment de modifier le comportement de chargement (ex: ajout de filtre).
---
layout: post
title: agf-release-test - Correction de la balise editCell
tags: [framework-1-79,codjo-release-test]
---
La méthode ```proceedTable``` de la classe ```EditCellStep``` a été corrigée de façon à ce que l'appel à la méthode ```editCellAt``` soit réalisé dans le thread ```Swing```.

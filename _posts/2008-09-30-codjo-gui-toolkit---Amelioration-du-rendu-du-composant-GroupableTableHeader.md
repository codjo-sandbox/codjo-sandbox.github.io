---
layout: post
title: agf-gui-toolkit - Amélioration du rendu du composant GroupableTableHeader
tags: [framework-1-64,codjo-gui-toolkit]
---
Correction du rendu du composant **GroupableTableHeader** dans le cas <u>où aucun header renderer n'est défini</u>:

Avant, une taille par défaut de hauteur était définie "en dur", ce qui limitait la possibilité d'afficher correctement plusieurs lignes dans le titre d'une colonne  .

Maintenant, la taille est calculée dynamiquement et l'affichage est correct. La correction a été effectuée dans la classe **GroupableTableHeaderUI**.
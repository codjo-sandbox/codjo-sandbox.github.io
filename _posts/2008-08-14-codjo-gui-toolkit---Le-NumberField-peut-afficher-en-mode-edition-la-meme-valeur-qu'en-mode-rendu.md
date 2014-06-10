---
layout: post
title: agf-gui-toolkit - Le NumberField peut afficher en mode édition la même valeur qu'en mode rendu
tags: [framework-1-57,codjo-gui-toolkit]
---
Le composant ```NumberField``` est un ```JTextField``` spécifique pour gérer des saisies de nombres. En mode saisie, il s'assure que l'utilisateur ne peut saisir que des nombres. De plus, il est possible de lui adjoindre un renderer pour gérer un affichage différent lorsque le composant n'est plus en édition.

Par exemple, si l'on installe un renderer qui filtre les 0 non-significatifs et que l'on saisit la valeur ```123.340000```, lorsque l'on validera la saisie, le composant affichera la valeur ```123.34```.

Par contre, lorsque l'utilisateur repasse en mode saisie, le renderer n'est pas appliqué et la valeur affichée est alors ```123.340000```.

Une méthode ```setApplyRendererInEditMode``` a été ajoutée sur le composant pour que le renderer s'applique aussi en mode édition. Par défaut, la valeur est configurée à ```false```.
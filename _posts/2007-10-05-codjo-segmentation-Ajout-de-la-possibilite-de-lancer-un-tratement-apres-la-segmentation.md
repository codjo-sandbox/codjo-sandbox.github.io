---
layout: post
title: agf-segmentation Ajout de la possibilité de lancer un tratement après la segmentation
tags: [framework-1-15,codjo-segmentation]
---
Ajout de la possibilité de lancer un traitement après la segmentation.

Pour cela il faut ajouter un paramètre dans la configuration de la segmentation :
&nbsp;\\
```
segmentationGuiPlugin.getConfiguration().
    setPostSegmentationTreatment("nomHandler");
```
Le handler aura accès :
* aux paramètres fournis à la segmentation (nom des paramètres définis dans l'application)
* et au resultat de la segmentation (nom du paramètre : status).
\\

Le handler est exécuté via une UpdateFactory.
\\
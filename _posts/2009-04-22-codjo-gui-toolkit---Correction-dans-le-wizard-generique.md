---
layout: post
title: agf-gui-toolkit - Correction dans le wizard générique
tags: [framework-1-92,codjo-gui-toolkit]
---
Modification de la méthode ```repaintStep``` dans ```WizardPanel``` :
* suppression d'appels inutiles à ```invalidate()``` et ```revalidate()```.
* utilisation de ```validate()``` sur le ```stepPanel``` (au niveau le plus fin).
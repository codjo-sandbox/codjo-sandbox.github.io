---
layout: post
title: agf-datagen - Amélioration de la génération
tags: [framework-1-104,codjo-datagen]
---
La partie datagen des projets est régénérée si une nouvelle version de la librairie ```codjo-datagen``` est déployée ou redéployée.

<u>Rappel</u>
La partie datagen est régénérée si :
* le fichier ```final.xml``` n'existe pas,
* les sources permettant de générer ```final.xml``` ont changé,
* une nouvelle version d'```codjo-datagen``` est déployée dans notre repository.


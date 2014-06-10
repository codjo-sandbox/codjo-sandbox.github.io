---
layout: post
title: agf-mad - L'entité définie dans les préférences est propagée au DetailDataSource
tags: [framework-1-95,codjo-mad]
---
Lors du chargement de la préférence de la ```RequestTable```, l'```entityName``` est transmis au ```ListDataSource```.

Il sera à présent transmis également au ```DetailDataSource``` lors de l'ouverture de l'écran-détail issu de la table.
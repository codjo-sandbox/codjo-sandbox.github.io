---
layout: post
title: agf-mad - Affichage d'une erreur en cas d'exception lors d'un ajout de ligne dans une RequestTable
tags: [framework-1-103,codjo-mad]
---
La méthode ```callRowFiller``` du ```ListDataSource``` bloquait explicitement les exceptions qui pouvaient résulter de l'appel au ```RowFiller``` défini dans une application. Un message apparaissait dans les logs mais ça nous a semblé insuffisant devant la gravité de l'erreur (en général, un mismatch entre les champs définis dans le ```RowFiller``` et le modèle de la base de données).

A présent, l'exception n'est plus bloquée par cette méthode et est véhiculée jusqu'au GUI où une boîte de dialogue apparait. De cette façon, l'erreur n'est plus masquée et peut être découverte au plus tôt.
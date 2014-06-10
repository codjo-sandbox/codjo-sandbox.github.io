---
layout: post
title: agf-datagen - Plus de génération des HandlerCommand
tags: [codjo-datagen,framework-1-17]
---
Suppression de la génération des handlers de type commande (relicat de l'ancienne plateforme).

Avec la nouvelle plateforme les handler de type commande ne sont plus générés, ce sont des classes java ajoutées dans le server, la génération de ces handlers n'a donc plus de sens dans la partie datagen.

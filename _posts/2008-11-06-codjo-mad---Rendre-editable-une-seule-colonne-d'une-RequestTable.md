---
layout: post
title: agf-mad - Rendre éditable une seule colonne d'une RequestTable
tags: [framework-1-68,codjo-mad]
---
Auparavant pour rendre une seule colonne éditable, il fallait rendre la table éditable en passant en paramètre la liste de toutes les colonnes non éditables.

Ajout dans RequestTable de la méthode setEditable(String... columns) permettant de rendre les colonnes listées éditables
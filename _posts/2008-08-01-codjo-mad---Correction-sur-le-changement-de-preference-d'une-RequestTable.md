---
layout: post
title: agf-mad - Correction sur le changement de préférence d'une RequestTable
tags: [framework-1-55,codjo-mad]
---
La méthode ```setPreference``` sur ```RequestTable``` était buggée dans le cas d'un changement dynamique de préférence en cours de vie d'une ```RequestTable```. Le modèle de la table n'était pas correctement mis à jour.
---
layout: post
title: agf-agent - Création d'un identifiant aussi unique que possible...
tags: [framework-1-65,codjo-agent]
---
La méthode ```IdUtil.createUniqueId(Object anObject)``` permet de créer un identifiant aussi unique que possible.

L'algo est basé sur l'utilisation :
* du hashCode de l'objet passé en paramètre
* d'un nombre tiré aléatoirement
* de la méthode ```System.currentTimeMillis()```
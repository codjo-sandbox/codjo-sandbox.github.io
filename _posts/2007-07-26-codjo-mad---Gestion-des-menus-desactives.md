---
layout: post
title: agf-mad - Gestion des menus désactivés
tags: [codjo-mad,framework-1-7]
---
Amélioration de la création des menus par la MenuFactory : lorsqu'un menu ou sous-menu contient exclusivement des entrées désactivées, il est lui-même automatiquement désactivé. Il n'est plus nécessaire de parcourir l'arbre après l'appel.
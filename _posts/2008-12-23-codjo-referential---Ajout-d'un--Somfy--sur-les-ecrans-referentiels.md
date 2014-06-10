---
layout: post
title: agf-referential - Ajout d'un "Somfy" sur les écrans référentiels
tags: [framework-1-77,codjo-referential]
---
Le plugin ```referentialGuiPlugin``` a été amélioré afin d'utiliser un ```waitingPanel``` lors du chargement du contenu des écrans référentiels.

L'option est débrayée par défaut, elle s'active via la configuration du plugin :

```
referentialGuiPlugin.getConfiguration().setWaitingPanel(true);
```

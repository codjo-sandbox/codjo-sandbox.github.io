---
layout: post
title: agf-gui-toolkit - Correction sur la gestion du model dans la classe TableMap
tags: [framework-1-77,codjo-gui-toolkit]
---
Correction du bug visible dans le cas d'un double appel à la méthode ```TableMap.setModel(...)```. Maintenant les listeners liés au précédent modèle sont nettoyés.

Ce bug apparaissait notamment lors de certaines utilisations d'un ```TableRendererSorter``` (e.g. test en échec sur ```codjo-segmentation```).

---
layout: post
title: agf-mad - RequestTableSum évènement lors de la mise à jour des valeurs
tags: [framework-1-73,codjo-mad]
---
Lors du recalcul des sommes, la table doit renvoyer un évènement.
Cela permet de déclencher les ```TableModelListener``` positionnés sur le modèle de la table.
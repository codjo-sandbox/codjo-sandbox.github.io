---
layout: post
title: agf-datagen - Correction requête SQL pour les handler delete
tags: [framework-1-62,codjo-datagen]
---
La requête construite automatiquement par datagen pour les ```handler-delete``` a été mise en conformité avec la norme ANSI.

Les requêtes générées suivent maintenant le pattern suivant : ```delete from MA_TABLE where PK=?```

 
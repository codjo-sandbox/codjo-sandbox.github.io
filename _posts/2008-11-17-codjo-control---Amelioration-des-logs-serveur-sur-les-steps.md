---
layout: post
title: agf-control - Amélioration des logs serveur sur les steps
tags: [framework-1-71,codjo-control]
---
Pour chaque ```step``` de contrôle ou de dispatch, une ligne a été ajoutée dans les logs serveur. Celle-ci précise :
- un statut indiquant si le ```step``` est exécuté ou non,
- le cas échéant, son temps d'exécution.
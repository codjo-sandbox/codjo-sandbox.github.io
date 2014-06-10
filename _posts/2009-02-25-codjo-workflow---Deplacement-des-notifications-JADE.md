---
layout: post
title: agf-workflow - Déplacement des notifications JADE
tags: [framework-1-84,codjo-workflow]
---
Les notifications Jade de début et de fin de traitements étaient envoyées avant la mise à jour dans la table d'audit ```AP_WORKFLOW_LOG```, maintenant nous envoyons ces notifications après avoir mis à jour la table d'audit.
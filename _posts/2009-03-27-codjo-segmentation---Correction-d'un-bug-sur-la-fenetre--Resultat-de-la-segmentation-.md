---
layout: post
title: agf-segmentation - Correction d'un bug sur la fenêtre "Résultat de la segmentation"
tags: [codjo-segmentation,framework-1-89]
---
Lorsque les résultats affichés sur cette fenêtre s'étalent sur plusieurs pages, et que l'on exécute les actions suivantes:

- Passage à la 2° page
- Modification du filtre en haut de la fenêtre  et clic sur le bouton "Go"

Si cette nouvelle recherche renvoie un résultat tenant sur une seule page, alors on se retrouve sur une 2° page qui est vide et qui n'a pas lieu d'être.

Ce bug est maintenant corrigé.
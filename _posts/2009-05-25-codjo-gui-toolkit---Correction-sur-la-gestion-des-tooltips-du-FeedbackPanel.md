---
layout: post
title: agf-gui-toolkit - Correction sur la gestion des tooltips du FeedbackPanel
tags: [framework-1-97,codjo-gui-toolkit]
---
Le ```FeedbackPanel``` permet d'ajouter des icônes dans le coin des composants graphiques pour attirer l'attention de l'utilisateur sur certaines parties d'IHM. Un tooltip est également ajouté pour expliquer la signification du symbole lié au composant.

L'API permet également de supprimer l'icône sur un composant. Dans ce cas, le tooltip de la légende n'était pas supprimé. Ce bug a été corrigé.
---
layout: post
title: agf-broadcast - Gestion des selectors génériques
tags: [framework-1-103,codjo-broadcast,hot-topics]
---
**{<u>}Contexte{</u>}** :
L'application Red permet de spécifier des "selectors" génériques d'export via une IHM (requête sql). Cette fonctionnalité permet d'appliquer des variations sur certains "selectors" sans devoir relivrer l'application.

**{<u>}Problème{</u>}** :
Les exports de Mint vers Roses, s'appuyant sur certaines caractéristiques des fonds, sont amenés à évoluer fréquemment. Dès lors, il a paru judicieux de réutiliser les "selectors" génériques de Red pour Mint.

**{<u>}Solution{</u>}** :
La librairie **codjo-broadcast** a été mise à jour pour gérer ce besoin.

**{<u>}Utilisation{</u>}** :
Une documentation est disponible : [[Utiliser les selector génériques]]

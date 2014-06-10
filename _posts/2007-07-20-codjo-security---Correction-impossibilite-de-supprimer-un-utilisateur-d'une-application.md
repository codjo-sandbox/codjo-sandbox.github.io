---
layout: post
title: agf-security - Correction impossibilité de supprimer un utilisateur d'une application
tags: [codjo-security,framework-1-6]
---
Bug [[5812@mantis]]

Le comportement de l'agent côté serveur qui effectuait la mise à jour du modèle de sécurité était le suivant :
* Un modèle de sécurité venant de la Bdd d'un côté
* Le nouveau modèle de sécurité venant du client

Le modèle de sécurité était parcouru par utilisateur, s'il n'existait pas dans le nouveau modèle alors il le rajoutait. En conséquence, l'utilisateur n'était jamais supprimé de la table PM_SEC_MODEL.

Cette opération a donc été supprimée.
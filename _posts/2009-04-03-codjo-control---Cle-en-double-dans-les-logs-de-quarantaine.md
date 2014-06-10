---
layout: post
title: agf-control - Clé en double dans les logs de quarantaine
tags: [framework-1-90,codjo-control]
---
Lors du renvoi des lignes de la quarantaine, une tentative d'insertion de clé en double dans la table des logs workflow (```AP_WORKFLOW_LOG```) empêchait l'ajout de la ligne concernant la dernière étape du traitement.

Cela a été corrigé.
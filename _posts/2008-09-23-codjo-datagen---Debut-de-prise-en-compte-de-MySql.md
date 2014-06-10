---
layout: post
title: agf-datagen - Début de prise en compte de MySql
tags: [framework-1-62,codjo-datagen]
---
Le module datagen a été modifié pour le rendre compatible avec MySql. Mais il reste à l'insérer proprement dans le mécanisme multi-base global.

Liste des modifications pour MySql : 
* Désactivation de la génération des triggers : pour le moment il est impossible de compiler des triggers en DEV (en cours de traitement)
* Les tables générées utilisent par défaut le moteur ```InnoDb``` (moteur transactionnel)
* Les handlers construits utilisent les mêmes spécificités que ORACLE.


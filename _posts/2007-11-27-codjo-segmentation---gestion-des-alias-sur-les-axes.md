---
layout: post
title: agf-segmentation - gestion des alias sur les axes
tags: [framework-1-21,codjo-segmentation]
---
Ajout de contrôles sur les alias des axes et notamment sur les cycles.
Suppression de l'axe courant dans la liste des axes disponibles pour les alias.
Modification du test des triggers (si noeud return devient si feuille alors).

Pour prendre en compte ces modifications, il faut relivrer les objets SQL dans l'ordre suivant :
* sp_SEG_Update_Includes.sql
* TR_PM_CLASSIFICATION_STRUCTURE_D.txt
* TR_PM_CLASSIFICATION_STRUCTURE_I.txt
* TR_PM_CLASSIFICATION_STRUCTURE_U.txt
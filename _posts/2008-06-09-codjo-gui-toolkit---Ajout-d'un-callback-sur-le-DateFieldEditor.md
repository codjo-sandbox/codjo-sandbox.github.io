---
layout: post
title: agf-gui-toolkit - Ajout d'un callback sur le DateFieldEditor
tags: [codjo-gui-toolkit,framework-1-47]
---
Lors de la saisie d'une date dans une table par la popup de calendrier, si l'utilisateur validait son écran, la date disparaissait (la valeur saisie était non validée).

Les composants DateField et DateFieldEditor ont été enrichis afin de pouvoir lancer un stopCellEditing sur la table lorsque l'utilisateur choisit une date via le calendrier.

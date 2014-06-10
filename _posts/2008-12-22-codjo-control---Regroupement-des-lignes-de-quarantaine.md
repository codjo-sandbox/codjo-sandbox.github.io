---
layout: post
title: agf-control - Regroupement des lignes de quarantaine
tags: [framework-1-77,codjo-control,hot-topics]
---
Un champ ```GROUP_ID``` est maintenant géré dans les IHM de quarantaine. Il permet de regrouper des lignes de quarantaine dans le but de les renvoyer en même temps via le bouton ```OK``` ou ```Forcer```. De cette façon, si l'utilisateur sélectionne une ligne dont le ```groupId``` est partagé par plusieurs lignes, l'ensemble des champs ```ERROR_TYPE``` de ces lignes seront modifiés en même temps.

La mise à jour de ce champ ```GROUP_ID``` s'effectue dans les steps de contrôle des plans d'intégration en fonction de critères "métier".

Le champ ```groupId``` doit être défini dans la structure de quarantaine de ```Datagen``` (```structure-quarantine.xml```).

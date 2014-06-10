---
layout: post
title: agf-control - Modification de la création du post audit
tags: [codjo-control,framework-1-14]
---
La construction de l'audit post-traitement est maintenant construite à partir des informations se trouvant dans la table de quarantaine au lieu de la table de contrôle temporaire. 

Ce changement est mis en place pour tenir compte des cas où les données du fichier d'entrée sont transposées en colonne dans la table de contrôle.


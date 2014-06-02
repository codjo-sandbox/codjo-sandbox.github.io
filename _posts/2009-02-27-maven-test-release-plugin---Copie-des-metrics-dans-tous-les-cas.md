---
layout: post
title: maven-test-release-plugin - Copie des métrics dans tous les cas
tags: [framework-1-85,maven-test-release-plugin]
---
Avant quand la variable ```-Dcoverage=true``` n'était pas positionnée, le plugin ne copiait pas les métriques sur ```:Z:\equipes\kaizen-tr\metrics```. Maintenant il le fait tout le temps. 

Pour info, les fichiers contenant l'ensemble des métriques (statistique + couverture) seront nommés ```metrics-<timestamp>-full.zip```


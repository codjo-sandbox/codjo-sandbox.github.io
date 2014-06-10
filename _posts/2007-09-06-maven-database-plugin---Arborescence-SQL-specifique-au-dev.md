---
layout: post
title: maven-database-plugin - Arborescence SQL spécifique au dév
tags: [framework-1-11,maven-database-plugin]
---
Il est possible de spécifier certains fichiers SQL à n'exécuter qu'en dév. Pour celà, les placer dans le répertoire /src/test/sql, avec la même structure que dans /src/main/sql. Cette arborescence ne sera exécutée qu'en mode dév, et ne sera pas livrée.
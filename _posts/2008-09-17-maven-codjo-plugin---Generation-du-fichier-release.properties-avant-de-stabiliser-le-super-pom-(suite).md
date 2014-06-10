---
layout: post
title: maven-agf-plugin - Génération du fichier release.properties avant de stabiliser le super-pom (suite)
tags: [framework-1-61,maven-codjo-plugin]
---
Lors de la stabilisation, à l'exécution du goal maven ```agf:release```, un fichier ```release.properties``` est généré (il contient la nouvelle version du framework, le tag associé et la version de développement du framework).

La liste des modules est maintenant obtenue à partir du projet maven (et non plus en dur dans le code).

Cf [[/2008/08/19/maven-codjo-plugin - Génération du fichier release.properties avant de stabiliser le super-pom]]

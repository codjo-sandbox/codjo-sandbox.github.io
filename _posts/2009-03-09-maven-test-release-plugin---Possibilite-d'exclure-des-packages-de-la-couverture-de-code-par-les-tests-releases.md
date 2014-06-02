---
layout: post
title: maven-test-release-plugin - Possibilité d'exclure des packages de la couverture de code par les tests-releases
tags: [framework-1-86,maven-test-release-plugin]
---
Il est à présent possible d'exclure des packages de la mesure de couverture de code par l'exécution des tests-releases.

Pour ce faire, il suffit de définir l'option ```-DpackagesToExclude=com.agf.mypackage1;com.agf.mypackage2``` en plus de l'option ```-Dcoverage=true``` lors de l'exécution des tests-releases en mode local.
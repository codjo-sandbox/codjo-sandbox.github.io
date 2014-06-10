---
layout: post
title: agf-pom - Correction pour exécution des tests release en snapshot
tags: [framework-1-67,codjo-pom]
---
Précédemment, 2 jars, qui étaient tirés par dépendance transitive par PdfBox, ont été exclues dans le super-pom. 

Ces exclusions ayant été faites après la dernière stabilisation du framework, la librairie codjo-release-test qui était en version stable 1.10 n'excluait pas ces 2 jars, ce qui entraînait des échecs de build pour les applications lors du lancement des tests release (les 2 jars ayant été supprimés du repository maven distant).

La librairie ```codjo-release-test``` a été passé en SNAPSHOT afin de pouvoir prendre en compte ces exclusions et ainsi pouvoir lancer les tests release lors d'un build.
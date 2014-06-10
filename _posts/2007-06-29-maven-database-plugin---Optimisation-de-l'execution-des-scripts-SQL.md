---
layout: post
title: maven-database-plugin - Optimisation de l'exécution des scripts SQL
tags: [maven-database-plugin,framework-1-4]
---
Une optimisation a été mise en place pour éviter de rejouer les scripts SQL (drop puis recréation de la Base de Données de développement) lorsque cela n'était pas nécessaire.
Si il n'y a pas de modification dans les fichiers Datagen ou dans les scripts SQL, alors la base n'est pas droppér et recréée.

Une conséquence de l'optimisation de la partie SQL est qu'il faudra faire un **mvn clean** pour forcer la Base de Données à se réinitialiser. (Cela devra se faire lors du passage d'une application à une autre application)
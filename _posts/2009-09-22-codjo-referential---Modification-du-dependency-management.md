---
layout: post
title: agf-referential - Modification du dependency management
tags: [framework-1-114,codjo-referential,resolution-of-brin]
---
{info}
Résolution de BRIN.
{info}

Le ```dependencyManagement``` de la librairie ```codjo-referential``` a été corrigé.
Les même dépendances que dans le ```super-pom``` ont été mises (suppression des classifiers ```client``` et ```serveur``` pour le module ```datagen```).

Cette modification corrige le problème rencontré lors de la suppression des tables ```PM_TABLE_LABEL``` et ```PM_COLUMN_LABEL``` dans ```codjo-mad``` qui n'avait pas fait échouer les tests release de ```agf-referential``` qui continuaient à référencer ces tables.

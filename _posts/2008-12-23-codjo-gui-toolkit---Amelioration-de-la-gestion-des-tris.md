---
layout: post
title: agf-gui-toolkit - Amélioration de la gestion des tris
tags: [framework-1-77,codjo-gui-toolkit]
---
La gestion des tris (```TableRendererSorter```) a été améliorée afin de mieux répondre aux événements. De plus l'émission d'événement a été optimisé afin d'éviter des "refresh" inutiles.

<u>Exemple</u> : Lors de la modification d'une ligne, l'indicateur de tri disparait lorsque la colonne impactée fait partie du tri existant, mais l'ordre visuel reste le même.

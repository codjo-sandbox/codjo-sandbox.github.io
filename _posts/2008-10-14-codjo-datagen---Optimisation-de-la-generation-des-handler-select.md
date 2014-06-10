---
layout: post
title: agf-datagen - Optimisation de la génération des handler-select
tags: [framework-1-66,codjo-datagen]
---
La génération des ```handler-select``` a été optimisée en extrayant le code commun dans une classe abstraite ```(AbstractSelectHandler```) se trouvant dans ```codjo-mad```.

<u>Exemple de gain</u> : Une classe générée est passée de 328 lignes à 68 lignes.


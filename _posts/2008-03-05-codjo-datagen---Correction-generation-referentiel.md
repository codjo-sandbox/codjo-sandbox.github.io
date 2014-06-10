---
layout: post
title: agf-datagen - Correction génération référentiel
tags: [codjo-datagen,framework-1-34]
---
Pour les référentiels héritant d'un autre référentiel, la description de l'entité n'était pas recopiée.
Cela impactait aussi le fichier ```structure.xml```

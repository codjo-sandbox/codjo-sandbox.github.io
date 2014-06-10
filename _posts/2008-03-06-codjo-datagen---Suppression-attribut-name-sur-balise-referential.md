---
layout: post
title: agf-datagen - Suppression attribut name sur balise referential
tags: [codjo-datagen,framework-1-34]
---
Nous avons supprimé l'attribut ```name``` sur la balise ```referential``` au niveau des ```entity``` gérant les référentiels générique (utilisés par Mint). Cet attribut était redondant avec la description de l'entity.

Suppression de l'attribut ```familyList``` de la balise ```referential``` du **datagen.xsd**
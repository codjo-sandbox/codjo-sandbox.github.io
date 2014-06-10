---
layout: post
title: agf-test - Nettoyage et cohérence XSD
tags: [codjo-test,framework-1-26]
---
Netoyage et resynchronisation du XSD avec les développements :
* Ajout des éléments manquants dans EditCell.
* Ajout d'éléments codés mais non déclarés dans le XSD.
* Ajout de contrainte sur attribut true/false.
* Suppression de la contrainte required sur l'attribut name des éléments pouvant être dans un EditCell.
* Alignement du XSD sur les attributs et simpleContent réellement acceptés par le code.

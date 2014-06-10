---
layout: post
title: agf-mad - Contrôle de la partie entière ajouté sur les champs de type nombre dans un DetailDataSource
tags: [framework-1-57,codjo-mad]
---
Les composants ```DetailDataSource``` configurent automatiquement les composants déclarés en fonction du type défini dans ```Datagen```. Si c'est un composant qui gère du texte, le nombre maximum de caractères autorisés à la saisie est configuré automatiquement. Si le composant gère des nombres, le nombre maximum de caractères autorisés dans la partie décimale est automatiquement configuré.

Suite au [[développement du contrôle du nombre maximum de caractères autorisés dans la partie entière sur le composant ```NumberField```|/2008/08/12/codjo-gui-toolkit - Contrôle du nombre de chiffres dans la partie entière d'un NumberField]], le ```DetailDataSource``` a été enrichi pour configurer ce nouveau contrôle automatiquement.
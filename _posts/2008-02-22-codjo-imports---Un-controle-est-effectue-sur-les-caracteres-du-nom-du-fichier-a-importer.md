---
layout: post
title: agf-imports - Un contrôle est effectué sur les caractères du nom du fichier à importer
tags: [codjo-imports,framework-1-32]
---
Lors des imports à la demande, afin d'éviter des problèmes avec VTOM, un contrôle est maintenant effectué sur le nom du fichier à importer.
Les caractères autorisés sont : **A** à **Z**, **a** à **z**, **0** à **9** et **. _ : / \ -**\\
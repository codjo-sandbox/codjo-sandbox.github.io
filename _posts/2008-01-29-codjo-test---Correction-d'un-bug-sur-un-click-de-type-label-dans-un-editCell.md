---
layout: post
title: agf-test - Correction d'un bug sur un click de type label dans un editCell
tags: [codjo-test,framework-1-28]
---
Le fait de cliquer sur un composant par son label et non par son nom à l'intérieur d'une balise editCell ne renvoyait pas d'erreur si le composant n'était pas trouvé. Ce bug est corrigé.

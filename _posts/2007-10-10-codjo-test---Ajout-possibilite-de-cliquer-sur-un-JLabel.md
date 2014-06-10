---
layout: post
title: agf-test - Ajout possibilité de cliquer sur un JLabel
tags: [codjo-test,framework-1-16]
---
La balise ```<click/>``` permet maintenant de cliquer sur un ```JLabel``` (en plus des ```JButton```).

Il y a aussi la possibilité de définir la politique de recherche de composant en se basant sur l'attribut "```matcher```". Deux valeurs sont possibles : "```equals```" (par défaut) et "```contains```"

Exemple : 
```xml
permettra de cliquer sur un ```JLabel``` ayant pour label "labol".  :)

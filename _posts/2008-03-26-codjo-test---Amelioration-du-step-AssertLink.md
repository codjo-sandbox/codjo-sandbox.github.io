---
layout: post
title: agf-test - Amélioration du step AssertLink
tags: [codjo-test,framework-1-37]
---
Ajout de la possibilité de vérifier la cible d'un lien avec l'attribut target dans le step assertLink.

Exemple : 
```
<assertLink target="url-cible.html">texte contenu dans le lien</a>
```
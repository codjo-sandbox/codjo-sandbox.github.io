---
layout: post
title: agf-aspect - Amélioration de la remontée d'erreur SQL lors de l'exécution d'un aspect
tags: [framework-1-78,codjo-aspect]
---
Lorsqu'un aspect était exécuté, si une ```SQLException``` se produisait, elle était englobée dans une ```AspectException```. Or, ```mad``` ne se basant que sur l'exception de plus haut niveau afin de générer le message d'erreur destiné au client, les informations relatives à la SQLException n'apparaissaient pas (le message d'erreur affiché au client était simplement **"Erreur SQL"** sans précision supplémentaire).

```title=AVANT
try {
...
}
catch (SQLException ex) {
   throw new AspectException("Erreur SQL", ex);
}
```

Maintenant, lorsque l'on catche une ```SQLException```, on renvoie une ```AspectException``` contenant le message de l'exception initiale afin que le message d'erreur affiché au client soit plus explicite.

```title=APRES
try {
...
}
catch (SQLException ex) {
   throw new AspectException("Erreur SQL : " + ex.getMessage(), ex);
}
```

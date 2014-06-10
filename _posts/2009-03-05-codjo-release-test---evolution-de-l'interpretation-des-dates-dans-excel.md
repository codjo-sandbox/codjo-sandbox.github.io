---
layout: post
title: agf-release-test - evolution de l'interprétation des dates dans excel
tags: [codjo-release-test,framework-1-86]
---
Evolution de l'assert Excel. Il est maintenant possible d'évaluer des cellules excel contenant la variable $TODAY avec du texte avant ou après.

Exemple:

```
TEXT BEFORE ${TODAY}+1D TEXT AFTER
```
---
layout: post
title: maven-delivery-plugin - Copie du livrable dans le dépot
tags: [framework-1-88,maven-delivery-plugin]
---
Le goal maven ```delreco```, utilisé lors du process de livraison d'une application, a été modifié pour prendre en compte le mode silencieux (option maven ```\--batch-mode```) : il fait alors automatiquement la copie du fichier zip dans le dépot DELRECO (sans poser la question).

```mvn delivery:delreco --batch-mode```
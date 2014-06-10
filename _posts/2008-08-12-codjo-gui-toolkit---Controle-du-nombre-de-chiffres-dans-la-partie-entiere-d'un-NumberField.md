---
layout: post
title: agf-gui-toolkit - Contrôle du nombre de chiffres dans la partie entière d'un NumberField
tags: [codjo-gui-toolkit,framework-1-56]
---
On peut préciser le nombre de chiffres acceptés dans la partie entière d'un ```NumberField```, en utilisant la méthode ```setMaximumIntegerDigits```.

Exemple:
```
numberField.setMaximumIntegerDigits(2);
```

Les valeurs suivantes sont acceptées : 10, 10.22, -10.23, -10
Les valeurs suivantes sont refusées : 110, 120.22, -120.23, -190

Les valeurs refusées font passer la couleur du texte en rouge.
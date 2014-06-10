---
layout: post
title: agf-gui-toolkit - Correction du TextFieldEditor
tags: [framework-1-82,codjo-gui-toolkit]
---
TextFieldEditor ne gère pas l'effacement du contenu de la cellule.

Celui-ci remplace dorénavant le contenu du model par "null" ainsi en base on retrouve bien une valeur <null> et non pas la chaine vide ""
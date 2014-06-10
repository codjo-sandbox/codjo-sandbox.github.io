---
layout: post
title: agf-gui-toolkit - ReadOnlyManager
tags: [codjo-gui-toolkit,framework-1-23]
---
Possibilité de désactiver la mise à jour de la valeur par défaut qui a été mise sur les composants graphiques.

Ajout de la méthode setReadOnly(boolean readOnly, boolean applyDefaultValues)

```
ReadOnlyManager readOnlyManager = ...;
readOnlyManager.setReadOnly(true, false);
``` 
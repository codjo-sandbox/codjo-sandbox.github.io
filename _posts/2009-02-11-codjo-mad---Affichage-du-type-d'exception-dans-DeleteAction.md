---
layout: post
title: agf-mad - Affichage du type d'exception dans DeleteAction
tags: [codjo-mad,framework-1-83]
---
Lorsqu'une erreur apparaît après une suppression, le message d'erreur contenait le type d'exception.

```Exemple : Impossible de supprimer ce numéro de compte(class com.agf.Aspect.AspectException)```

Il est maintenant possible de ne plus afficher le type d'exception en agissant sur la classe ```DeleteAction``` à l'aide de la méthode suivante:

```
public void setDisplayErrorType(boolean displayErrorType)
```

Par défaut, le type d'exception est affiché.
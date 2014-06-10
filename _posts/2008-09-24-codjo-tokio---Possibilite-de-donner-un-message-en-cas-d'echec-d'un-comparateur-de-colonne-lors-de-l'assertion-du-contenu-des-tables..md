---
layout: post
title: agf-tokio - Possibilité de donner un message en cas d'échec d'un comparateur de colonne lors de l'assertion du contenu des tables.
tags: [framework-1-60,codjo-tokio]
---
Dans un fichier Tokio il est possible de préciser, à l'aide de la balise ```<comparator>```, un comparateur spécifique pour une colonne d'une table à utiliser lors d'un ```tokio-assert``` ou ```verifyAllOutputs```.

On peut maintenant, en cas d'échec de la comparaison, donner la cause d'échec à l'aide de la méthode ```getReason``` :

```
public interface Comparator {
   ...
   String getReason();
   ...
}
```

Le message est affiché dans le message d'erreur, après la valeur attendue et réelle de la colonne :

Sans message : 
```
[[COL_DATE]] expected = (2002-12-20 00:00:00.0)  valeur   = (9999-12-20 00:00:00.0)
```
Avec message : 
```
[[COL_DATE]] expected = (2002-12-20 00:00:00.0)  valeur   = (9999-12-20 00:00:00.0) : Mauvais millénaire
```

Ceci permet de donner une indication plus précise à l'utilisateur dans le cas où le comparateur ne vérifie pas l'égalité simple des valeurs.
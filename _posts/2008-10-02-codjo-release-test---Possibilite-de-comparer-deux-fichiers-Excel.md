---
layout: post
title: agf-release-test - Possibilité de comparer deux fichiers Excel
tags: [framework-1-64,codjo-release-test]
---
La tâche assert-excel a été étendue pour permettre de comparer deux fichiers Excel.

Un nouvel attribut facultatif a été ajouté : ```actual```, qui précise le nom d'un fichier à comparer. Si l'attribut n'est pas présent, le comportement est identique au comportement précédent (le fichier ```expected``` est comparé au fichier ouvert dans Excel au moment de l'appel de la balise).

Exemple :
```
<assert-excel expected="expected.xls" actual="actual.xls" rowCount="42" columnCount="9"/>
```

Doc : [[assert-excel]]
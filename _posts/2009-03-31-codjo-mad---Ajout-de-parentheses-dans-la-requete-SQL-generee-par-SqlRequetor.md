---
layout: post
title: agf-mad - Ajout de parenthèses dans la requête SQL générée par SqlRequetor
tags: [framework-1-89,codjo-mad]
---
Des parenthèses ont été rajoutées, dans la clause "where" de la requête SQL générée par la classe SqlRequetor, entre le terme "mandatoryClause" et les termes choisis par l'utilisateur.

A titre d'exemple, avant cette modification, cette classe générait la requête suivante

```
SELECT champ1, champ2
FROM maTable
WHERE
mandatoryClause
AND champ1='toto'
OR champ2='fred'
```

tandis que maintenant, on obtient la requête suivante :

```
SELECT champ1, champ2
FROM maTable
WHERE
mandatoryClause
AND ( champ1='toto'
OR champ2='fred' )
```

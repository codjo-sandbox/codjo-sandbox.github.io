---
layout: post
title: agf-release-test - Possibilité de spécifier les feuilles Excel à comparer dans la balise AssertExcel
tags: [framework-1-111,codjo-release-test,hot-topics]
---
Il est maintenant possible de spécifier les feuilles Excel que l'on souhaite comparer. Il suffit d'utiliser l'attribut ```sheets``` avec la liste des feuilles séparées par ```,```.
Si l'attribut n'est pas précisé, la comparaison portera sur tout le fichier.

<u>Exemple:</u>
```
<assert-excel expected="excelFile.xls" sheets="feuille1,feuille2"/>
```
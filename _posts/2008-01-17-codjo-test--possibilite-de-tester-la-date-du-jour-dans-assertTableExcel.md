---
layout: post
title: agf-test -possibilité de tester la date du jour dans assertTableExcel
tags: [framework-1-27,codjo-test]
---
Lors de l'utilisation de la balise <assertTableExcel>,
il est désormais possible de comparer une colonne contenant la date du jour.

Pour cela, il faut mettre dans le fichier Excel contenant l'étalon, la variable:
```
${TODAY}
```


Petite précision : la date du jour attendu dans la table doit être au fromat dd/MM/yyyy.
\\
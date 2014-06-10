---
layout: post
title: agf-mad - Evolution sur les renderer dans SelectionGui
tags: [framework-1-100,codjo-mad]
---
Dans le composant ```SelectionGui```, si l'on paramètre une préférence avec des renderer spécifiques sur la table de gauche (```fromTable```), ces renderers étaient perdus et remplacés par ```ListSelectionRenderer``` qui ne fait que changer la couleur de fond des lignes.

Dans la classe ```ListSelectionRenderer```, Un constructeur a été ajouté, auquel il est possible de passer un renderer.

```
public ListSelectionRenderer(SelectionLogic logic, TableCellRenderer tableRenderer)
```

En plus du grisage des lignes, les renderers indiqués dans la préférence de la ```fromTable``` pourront être ainsi conservés.

La classe SelectionLogic a été modifiée afin qu'un renderer de type ```PreferenceRenderer``` soit conservé dans la ```fromTable```
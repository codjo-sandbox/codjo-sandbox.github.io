---
layout: post
title: agf-gui-toolkit - GroupableTableHeader
tags: [framework-1-20,codjo-gui-toolkit,hot-topics]
---
- Possibilité d'ajouter des regroupements de colonnes sur le Header d'une JTable pour une visualisation de l'entête de la table plus lisible sur plusieurs lignes.\\

Un builder est disponible pour faciliter la construction du composant :
```
        GroupableTableHeaderBuilder.install(table)
              .createGroupColumn("Name", 1, 2)
              .createGroupColumn("Language", 3, 4)
              .createGroupColumn("Others", 5, 6)
              .createGroupColumn("Currency", 7, 8, 9, 10)
              .build();
```

Ici, on crée :
- un groupe de colonnes nommé "Name" contenant les colonnes d'indice 1 et 2.
- un groupe de colonnes nommé "Language" contenant les colonnes d'indice 3 et 4.
- un groupe de colonnes nommé "Others" contenant les colonne 5 et 6.
- un groupe de colonnes nommé "Currency" contenant les colonnes d'indice 7, 8, 9 et 10.
L'appel à la méthode build() construit alors le composant.

Le composant permet aussi d'ajouter un niveau supplémentaire de regroupement de colonnes. Ceci est expliqué de manière plus détaillée sur la page [[GroupableTableHeader]]

---
layout: post
title: agf-gui-toolkit - Amélioration de la synchronisation des colonnes de différentes tables
tags: [codjo-gui-toolkit,framework-1-64]
---
La synchronisation du redimensionnement des largeurs de colonnes de différentes JTables et la synchronisation du déplacement de ces colonnes a été améliorée.
Cette amélioration permet désormais de ne plus devoir spécifier une JTable maître et un tableau de JTables esclaves. Il est désormais possible de passer simplement un tableau de JTables à synchoniser.
En conséquence, la synchronisation des JTables se fait en jouant sur le header de n'importe laquelle de ces tables (et non plus uniquement sur le header de la table maître).

L'accès public à l'ancienne méthode de synchronisation n'a pas été supprimée pour l'instant (Utilisations : codjo-mad et Mint).

```title=Ancienne méthode de synchronisation
JTable masterTable;
JTable[[]] slaveTables;
...
TableUtil.synchronizeColumns(masterTable, slaveTables);
```

\\
```title=Nouvelle méthode de synchronisation
JTable[[]] synchronizedTables;
...
TableUtil.synchronizeTableColumns(synchronizedTables);
```

NB : Le nom de la méthode est différent pour éviter les signatures ambigües que peuvent entraîner l'utilisation des ellipses.
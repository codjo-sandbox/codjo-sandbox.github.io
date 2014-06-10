---
layout: post
title: agf-mad - Preference - La liste de String hiddenColumns devient une liste de Column
tags: [codjo-mad,framework-1-45,hot-topics]
---
Dans les préférences, la liste des colonnes cachées étaient une liste ds String contenant les "fieldName" des colonnes cachées. C'est désormais une liste de colonne.

Il est maintenant possible
* de cacher une colonne en appelant la méthode:
```
public void hideColumn(Column column)
```

* d'afficher une colonne à la fin de la table en appelant la méthode:
```
public void displayColumn(Column column)
```

* d'afficher une colonne à une position donnée en appelant la méthode:
```
public void displayColumn(int position, Column column)
```

* de spécifier un label, une taille, ... dans le fichier preference.xml
```
<hidden>
	<column fieldName="codeInstrument" label="Code Instrument" preferredSize="50"/>
</hidden>
```
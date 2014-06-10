---
layout: post
title: agf-mad - Séparateur décimal dans l'export Excel
tags: [codjo-mad,framework-1-109,hot-topics]
---
Il est maintenant possible de spécifier le caractère que l'on souhaite utiliser comme séparateur décimal dans un export Excel.

Par exemple, pour utiliser une virgule comme séparateur décimal, ajouter la ligne suivante dans le fichier ```application.properties``` du module ```gui``` du projet:
```
mad.export.excel.decimalSeparator = ,
```

Dans la préférence correspondante, il faut que le champ en question possède l'attribut ```sorter``` et soit égal à ```Numeric```

```xml
...
<preference id="MachinList">
...
    <column fieldName="rate" label="Taux" sorter="Numeric"/>
...
</preference>
...
```

{info:title=Attention}
Ce paramétrage est valable sur tous les exports Excel de l'application
{info}
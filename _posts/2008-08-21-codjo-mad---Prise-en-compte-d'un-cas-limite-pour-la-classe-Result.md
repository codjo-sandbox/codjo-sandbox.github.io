---
layout: post
title: agf-mad - Prise en compte d'un cas limite pour la classe Result
tags: [framework-1-58,codjo-mad]
---
Modification des méthodes ```getRow``` et ```rowContainsField``` afin de pouvoir gérer le cas où la variable interne **rows** (représentant la liste des lignes) serait égale à **null**.

&nbsp;Le code source de ces méthodes est le suivant :\\
```
     public Row getRow(int row) {
        List<Row> rows = this.getRows();
        return (rows != null ? rows.get(row) : null);
    }

    public boolean rowContainsField(int row, String fieldName) {
        Row fields = getRow(row);
        return (fields != null && fields.contains(fieldName));
    }
```\\ \\
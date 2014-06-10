---
layout: post
title: agf-mad - Ajout d'une mécanique de comparaison globale sur RequestTable
tags: [codjo-mad,framework-1-10]
---
RequestTable gère à présent la possibilité de brancher un tri global sur la table par la méthode "setRowComparator(RowComparator comparator)".
&nbsp;
L'interface RowComparator fournit les Row du DataSource associé à la table permettant ainsi de définir une politique de comparaison ligne à ligne sur le DataSource.
\\
```
public interface RowComparator extends Comparator<Row> {
    int compare(Row row1, Row row2);
}
```
L'exemple suivant illustre cette mécanique. Le comparator branché sur la table effectue un tri sur les lignes en fonction de la valeur de la colonne "code" (en première position dans la table). A noter que le fait de brancher un RowComparator global désactive le tri par colonne sur la table.&nbsp;
```
table.setRowComparator(new RowComparator() {
    public int compare(Row row1, Row row2) {
        Integer row1Priority = new Integer(row1.getFieldValue("code"));
        Integer row2Priority = new Integer(row2.getFieldValue("code"));
        return row1Priority.compareTo(row2Priority);
    }
});
```
Le fonctionnement de la mécanique est décrit ci-dessous sous forme de test unitaire.
\\
```
assertTrue(testTable.contentEquals(new Object[[][]]{
    {"1", "isinVal1", "sicovamVal1"},
    {"2", "isinVal2", "sicovamVal2"},
    {"3", "isinVal3", "sicovamVal3"},
}));

table.getDataSource().setValue(0, "code", "4");
table.sort();
 
assertTrue(testTable.contentEquals(new Object[[][]]{
    {"2", "isinVal2", "sicovamVal2"},
    {"3", "isinVal3", "sicovamVal3"},
    {"4", "isinVal1", "sicovamVal1"},
}));
```
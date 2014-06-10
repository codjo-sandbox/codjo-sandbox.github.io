---
layout: post
title: agf-gui-toolkit - ScrollPane étendu
tags: [codjo-gui-toolkit,framework-1-83,hot-topics]
---
Un ScrollPane plus évolué a été ajouté. Il permet de pouvoir définir des ```JComponent``` au niveau des ```Viewport``` en bas et à droite. (sur la capture d'écran ci dessous,  il s'agit des 2 ```JTable``` sur fonds bleu ont été ajoutées à ces positions).

![Alt attribute text Here](attachments/SoScrollPane.png)


Cette implémentation permet, entre autre, de pouvoir définir des ```JTables``` dont les scrolls verticaux et horizontaux sont synchronizés. Il est ainsi possible de conserver la vue sur les colonnes/lignes situées aux extrémités.


Les vues gérées par ce scrollPane se schématisent de la manière suivante :
![Alt attribute text Here](attachments/ExtendedScrollPaneRegions.JPG)


Pour pouvoir définir un composant dans une de ces vues, il faut utiliser une des méthodes suivantes :
<table>
<tr>
<th>Method</th><th>View</th><th>Comment</th></tr>
<tr>
<td> setViewportView(JComponent component)     </td>
<td> Center </td>
<td> Identique au JScrollPane </td>
</tr>
<tr>
<td> setRowHeaderView(JComponent component)    </td>
<td> RowHeader </td>
<td> Identique au JScrollPane </td>
</tr>
<tr>
<td> setColumnFooterView(JComponent component) </td>
<td> ColumnFooter </td>
<td> Spécifique au ExtendedScrollPane </td>
</tr>
<tr>
<td> setRowFooterView(JComponent component)    </td>
<td> RowFooter </td>
<td> Spécifique au ExtendedScrollPane </td>
</tr>
</table>


Voici une partie de l'exemple de code permettant d'utiliser des ```JTable``` positionnées dans les différentes vues.
```
private JScrollPane createScrollPane() {
        ExtendedScrollPane pane = new ExtendedScrollPane();
        pane.setHorizontalScrollBarPolicy(JScrollPane.HORIZONTAL_SCROLLBAR_ALWAYS);
        pane.setVerticalScrollBarPolicy(JScrollPane.VERTICAL_SCROLLBAR_ALWAYS);

        JTable mainTable = createMainTable();
        JTable footerTable = createFooterTable();
        TableUtil.synchronizeTableColumns(mainTable, footerTable);
        JTable rowHeaderTable = createRowHeaderTable();
        JTable rowFooterTable = createRowFooterTable();
        TableUtil.synchronizeTableSelection(ListSelectionModel.SINGLE_SELECTION,
                                            mainTable, rowHeaderTable, rowFooterTable);

        pane.setViewportView(mainTable);
        pane.setRowHeaderView(rowHeaderTable);
        pane.setColumnFooterView(footerTable);
        pane.setRowFooterView(rowFooterTable);

        pane.setCorner(JScrollPane.UPPER_LEFT_CORNER, createPanel(Color.YELLOW, "Upper Left"));
        pane.setCorner(JScrollPane.UPPER_RIGHT_CORNER, createPanel(Color.YELLOW, "Upper Right"));
        pane.setCorner(JScrollPane.LOWER_LEFT_CORNER, createPanel(Color.YELLOW, "Lower Left"));
        pane.setCorner(JScrollPane.LOWER_RIGHT_CORNER, createPanel(Color.YELLOW, "Lower Right"));

        return pane;
    }
```

{info:title=Application possible au composant RequestTableSum}
La ```RequestTableSum``` pourrait ainsi être refactorée en un composant unique contenu dans un scrollPane unique.
{info}
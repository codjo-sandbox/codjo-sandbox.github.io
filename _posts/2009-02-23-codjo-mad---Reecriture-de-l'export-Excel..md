---
layout: post
title: agf-mad - Réécriture de l'export Excel.
tags: [framework-1-84,codjo-mad]
---
<u>Problème</u>:

Auparavant l'export Excel de plusieurs tables n'était pas souple, car implémenté pour répondre à un besoin spécifique de Mint.
En effet, il était présupposé que toutes les tables exportées avaient la même structure (cf. frais de gestion Mint), donc un seul en-tête était affiché pour toutes les tables.
Dès lors il n'était pas possible d'exporter plusieurs tables avec des structures différentes.

<u>Solution</u>:

La réécriture de la classe **ExcelFunction** en **ExportExcelBuilder** permet à présent d'afficher autant d'en-têtes que de tables, avec la possibilité d'afficher plusieurs en-têtes pour chaque table.

<u>Utilisation</u>:

Pour réaliser une action qui effectuera un export excel de plusieurs tables il faut étendre **ExportAction**.
Par défaut elle permet d'exporter toutes les tables avec leur en-tête de colonnes respectif.
```
public ExportAllTablesAction(GuiContext ctxt, RequestTable... table) {
        super(ctxt, table);
}
```
Résultat :
![Alt attribute text Here](attachments/exportExcelMultiTable.jpg)

Si l'on désire ajouter/modifier un ou plusieurs en-têtes pour certaines tables, alors il faut surcharger la méthode _setTableHeaderForBuilder_ et ajouter chaque table et ses en-têtes associés dans l'ordre souhaité:
```
    public ExportAllTablesAction(GuiContext ctxt, RequestTable... table) {
        super(ctxt, table);
        builder.setRenderValueFunctor(new FeesRenderValueFunctor());

    }

    @Override
    protected void setTableHeaderForBuilder(RequestTable... table) {
        builder.setHeaderData(table[[0], ExportExcelBuilder.createColumnHeader(table[0]]),
                    new Object[[][]]```"Frais de gestion directs"```)
               .setHeaderData(table[[1], new Object[][]]```"Frais de gestion indirects"```)
               .setHeaderData(table[[2], new Object[][]]```"Autres frais de gestion"```);

    }
```

<u>Remarques</u>:
La méthode statique _createColumnHeader_ de l' **ExcelExportBuilder** permet de créer l'en-tête des colonnes.

De plus, un **RenderValueFunctor** peut être spécifié au builder.
Il permet de récupérer la valeur en fonction du renderer appliqué aux colonnes.
```
private static class FeesRenderValueFunctor implements RenderValueFunctor {

        public Object getRenderedValue(RequestTable jTable, int row, int col) {
            TableCellRenderer renderer =
                  jTable.getCellRenderer(row, jTable.convertColumnIndexToView(col));

            Object value = jTable.getValueAt(row, col);
            if (renderer != null) {
                Component component = renderer
                      .getTableCellRendererComponent(jTable, value, false, false, row, col);
                if (component instanceof JLabel) {
                    return ((JLabel)component).getText();
                }
                else if (component instanceof JButton) {
                    return "A " + ((JButton)component).getText();
                }

               ...
```

Résultat :
![Alt attribute text Here](attachments/exportExcelMultiTable_custom.jpg)

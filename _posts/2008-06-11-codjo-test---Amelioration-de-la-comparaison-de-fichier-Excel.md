---
layout: post
title: agf-test - Amélioration de la comparaison de fichier Excel
tags: [codjo-test,framework-1-48]
---
La comparaison de fichier excel qui ne tenait compte auparavant que des valeurs, tient maintenant compte :
* Des cellules fusionnées
* Des styles appliqués aux cellules:
**** Alignement : général, gauche, centré, droite, justifié
**** Styles : Gras; italic
**** Bordures de cellules
* Des marges d'impression

Ajout d'une interface ```CellStringifier``` permettant de découpler la comparaison des valeurs et des styles, ce qui permet un débrayage de la comparaison de styles.

```public interface CellStringifier {
    public String toString(Cell cell);
}```

Utilisation dans les assertions dans la classe ```ExcelComparisonStrategy``` :
```    private void assertSheetContent(int index,
                                    HSSFWorkbook expectedWorkbook,
                                    HSSFWorkbook actualWorkbook) {
        assertCells("Contenu de la feuille",
                    index, expectedWorkbook, actualWorkbook,
                    new CellValueStringifier(),
                    new CellValueStringifier());
    }```

La comparaison de style est embrayable dans le code des TU de la manière suivante :
```fileAssert.setCompareStyle(true);```
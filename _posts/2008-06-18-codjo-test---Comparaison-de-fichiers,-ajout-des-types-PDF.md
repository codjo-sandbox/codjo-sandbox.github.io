---
layout: post
title: agf-test - Comparaison de fichiers, ajout des types PDF
tags: [codjo-test,framework-1-49]
---
Ajout de la classe ```PDFComparisonStrategy``` permettant de comparer des fichiers de type PDF en utilisant la librairie PDFBox-0.7.3

Modification de la méthode ```fileAssert.execute```

```
try {
  if (expected.endsWith(".xls")) {
    info("\tUse Excel comparison strategy...");
    assertFile(new ExcelComparisonStrategy(getExpectedFile(), getActualFile(), compareStyle));
 }
 else if(expected.endsWith(".pdf")){
    info("\tUse PDF comparison strategy...");
    assertFile(new PDFComparisonStrategy(getExpectedFile(), getActualFile()));

 }
[[...]]
```

comparaison :
* textuelle du contenu
* des polices de caractères utilisées
* des images (nombre d'images, taille des images)
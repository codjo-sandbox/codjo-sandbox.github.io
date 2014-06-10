---
layout: post
title: agf-segmentation - Ajout du module d'export de paramétrage
tags: [framework-1-24,codjo-segmentation]
---
Ce module permet d'exporter tous les Axes et/ou toutes les Poches stockés en base dans un fichier texte (.txt) séparé par des tabulations. Les formats des fichiers exportés sont les mêmes que ceux destinés à l'import.

Afin de pouvoir utiliser cet export dans une application, il faut ajouter dans le menu.xml :
```
<menu plugin="com.agf.segmentation.gui.plugin.SegmentationGuiPlugin" actionId="ExportParametersAction"/>
```


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
Si vous utilisez les modules d'export / import pour transférer des axes d'un environnement à un autre, les alias d'axe par pointeurs (includes) pourront ne plus fonctionner car ils s'appuient sur une colonne non gérée par ceux-ci (SLEEVE_ROW_ID) et contenant le timestamp de création de la poche.
</p></td>
          </tr>
</table>


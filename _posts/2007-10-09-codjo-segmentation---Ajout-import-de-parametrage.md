---
layout: post
title: agf-segmentation - Ajout import de paramétrage
tags: [codjo-segmentation,framework-1-15]
---
Cet import permet d'intégrer des Axes et des Poches à partir d'un fichier texte séparé par tabulations.

Afin de pouvoir utiliser cet import dans une application, il faut :

Dans le menu.xml :
```
<menu plugin="com.agf.segmentation.gui.plugin.SegmentationGuiPlugin"
actionId="ImportParametersAction"/>
```

Dans Datagen :
```
<include>com.agf.segmentation.gui.importParam.ImportParametersAction</include>
```
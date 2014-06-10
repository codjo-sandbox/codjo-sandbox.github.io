---
layout: post
title: agf-release-test - Assert sur la couleur de fond d'une JTable
tags: [framework-1-71,codjo-release-test]
---
Un attribut **background** a été ajouté à la balise **<assertTable>** afin de vérifier la couleur de fond de la cellule.
La couleur attendue est spécifiée sous la forme RGB.
\\

Exemple :
```
<assertTable name="colorCodingTable" row="2" column="Isin" expected="FR00001" background="255,102,0"/>
```
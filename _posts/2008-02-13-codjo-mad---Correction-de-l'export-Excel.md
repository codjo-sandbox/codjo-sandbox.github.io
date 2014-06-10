---
layout: post
title: agf-mad - Correction de l'export Excel
tags: [codjo-mad,framework-1-31]
---
L'export Excel d'une ```RequestTable``` ne prenait en compte que la dernière page.

La sauvegarde/restitution de la page courante avant export qui était faite dans ```ExportAllPagesAction.actionPerformed(...)``` a été déplacée dans ```ExcelFunctions.allPagesToExcel(...)```.
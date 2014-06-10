---
layout: post
title: agf-mad - Modification sur export Excel
tags: [codjo-mad,framework-1-26]
---
Export Excel : ajout des méthodes **createExtraHeaderData()** et **createHeaderData()** permettant de customiser les données exportées.

**createHeaderData()** : permet de customiser les données du header lors de l'export Excel. Par défaut, les données d'un header classique **JTableHeader** et d'un **GroupableTableHeader** sont exportées.

**createExtraHeaderData()** permet d'ajouter des données à l'export Excel. Ces données sont ajoutées entre les données du header et les données contenues dans la table.
---
layout: post
title: agf-mad - Correction sur l'export Excel
tags: [framework-1-85,codjo-mad]
---
Problème :
La création de l'en-tête des tables à exporter s'effectuait lors de l'instanciation de l'action ExportAction. Du coup l'export ne prenait pas en compte d'éventuelles manipulations des colonnes des tables.

Correction :
A présent la génération des en-têtes s'effectuera lors de la demande d'export.

Voir [[News|http://wp-confluence/confluence/pages/viewpage.action?pageId=10944518]] pour la customisation des en-têtes.
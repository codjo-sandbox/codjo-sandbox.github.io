---
layout: post
title: agf-plugin - Amélioration du log d'erreur des scripts import et export.ksh
tags: [framework-1-82,codjo-plugin]
---
Modification des scripts import/export.ksh en complément des modifications apportées et décrites dans une news précédente: [[http://wp-confluence/confluence/pages/viewpage.action?pageId=9504456]]

Modifications apportées:
\- Les erreurs sont concaténées dans les fichiers _"import_error.txt" / "export_error.txt",_ au lieu d'être écrasées à chaque fois.

\- Ces fichiers sont désormais dans le répertoire de log de l'application concernée dont le chemin est défini dans le pom racine grâce à la variable _logDir_.
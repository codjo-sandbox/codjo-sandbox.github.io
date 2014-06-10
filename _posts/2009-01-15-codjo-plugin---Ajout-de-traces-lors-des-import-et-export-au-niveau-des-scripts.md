---
layout: post
title: agf-plugin - Ajout de traces lors des import et export au niveau des scripts
tags: [framework-1-79,codjo-plugin]
---
**{<u>}Contexte{</u>}**: Plusieurs plantages de MINT sur Hudson&nbsp; apparaissent de manière chronique sur les tests release des imports et exports, avec des problèmes notamment de "FileNotFoundException" **non reproductibles localement**.

Les imports se font via le lancement des scripts _import.ksh_ et _export.ksh._

En cas d'erreur lors de l'exécution, ces scripts ne renvoient pas de message d'erreur, donc impossible de savoir ce qu'il se passe.

**{<u>}Action{</u>}**: Modification des scripts pour logguer les plantages.

A chaque plantage de l'exécution de ces scripts on récupère le numéro d'erreur que l'on affiche dans les logs, et on logge le message d'erreur dans un fichier _"import_error.txt" / "export_error.txt",_ avec la date, le nom du fichier et l'initiateur du batch.
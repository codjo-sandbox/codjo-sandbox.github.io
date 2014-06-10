---
layout: post
title: agf-plugin - Correction du fichier import.ksh
tags: [hot-topics,framework-1-107,codjo-plugin]
---
Dans le cas où le batch était en erreur, le code retourné n'était pas remonté par le ksh et donc VTom ne détectait aucune erreur. 

Cela a été corrigé.
---
layout: post
title: agf-confluence - Correction du téléchargement des pièces jointes
tags: [codjo-confluence,framework-1-47]
---
La méthode ```downloadAttachment``` dans ```ConfluenceServer``` ne sauvegardait pas bien les fichiers récupérés depuis Confluence.
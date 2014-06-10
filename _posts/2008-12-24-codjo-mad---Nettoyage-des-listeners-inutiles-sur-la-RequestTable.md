---
layout: post
title: agf-mad - Nettoyage des listeners inutiles sur la RequestTable
tags: [framework-1-77,codjo-mad]
---
Dans certains cas, des listeners inutiles liés au ```TableRendereSorter``` restaient actifs.
Ils sont désormais supprimés.
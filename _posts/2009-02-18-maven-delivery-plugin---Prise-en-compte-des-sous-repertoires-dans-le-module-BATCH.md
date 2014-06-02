---
layout: post
title: maven-delivery-plugin - Prise en compte des sous-repertoires dans le module BATCH
tags: [framework-1-83,maven-delivery-plugin]
---
Une évolution a été apportée afin de prendre en compte, dans le repertoire **script**, les structures du type :
```
|-- script
    |
    |-- windows
    |   |
    |   |-- myBatch.cmd
    |
    |-- unix
        |
        |-- myBatch.ksh
```
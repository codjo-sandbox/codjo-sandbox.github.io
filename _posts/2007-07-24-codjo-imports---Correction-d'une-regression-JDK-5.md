---
layout: post
title: agf-imports - Correction d'une regression JDK 5
tags: [framework-1-6,codjo-imports]
---
Le message suite à une erreur de formattage d'un nombre est parfois inexplicite (i.e. ```'null'```). Dans ces cas limites, la valeur en erreur est précisée.
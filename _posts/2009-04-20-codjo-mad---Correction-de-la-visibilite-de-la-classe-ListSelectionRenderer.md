---
layout: post
title: agf-mad - Correction de la visibilité de la classe ListSelectionRenderer
tags: [framework-1-92,codjo-mad]
---
<u>Problème</u>
La visibilité de la classe ```ListSelectionRenderer``` était **publique** alors que celle de ses constructeurs était niveau **package**.

<u>Correction</u>
A présent, la classe ```ListSelectionRenderer``` est visible au niveau **package**.
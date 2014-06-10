---
layout: post
title: agf-mad - Prise en compte des cas limites pour Result.containsField()
tags: [framework-1-66,codjo-mad]
---
La méthode ```Result.containsField(rowIndex, fieldName)``` lance désormais une exception ```IndexOutOfBoundsException``` dans les cas limites (e.g. index négatif).

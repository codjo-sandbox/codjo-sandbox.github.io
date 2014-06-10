---
layout: post
title: agf-mad - Prise en compte des cas limites pour Result.containsField()
tags: [framework-1-62,codjo-mad]
---
La méthode ```Result.containsField(rowIndex, fieldName)``` retourne désormais ```false``` dans les cas limites (e.g. index négatif).

<u>Exemple</u>: 
```java
Result result = new Result(primaryKeys, row("label", "euro"));

assertTrue(result.containsField(0, "label"));           // Champs présent => OK
assertFalse(result.containsField(0, "unknownColumn"));  // Champs inconnu => KO   
assertFalse(result.containsField(625, "label"));        // Ligne inconnue => KO
```

**Pour Info** : Les méthodes ```rowContainsField(...)``` et ```contains(...)``` ont été respectivement supprimées et dépréciées. Elles sont remplacées par la nouvelle méthode ```containsField(...)```.
 

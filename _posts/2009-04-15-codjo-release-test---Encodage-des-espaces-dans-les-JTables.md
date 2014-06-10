---
layout: post
title: agf-release-test - Encodage des espaces dans les JTables
tags: [framework-1-91,codjo-release-test]
---
Lors de l'assertTableExcelStep, dans la méthode assertExpectedValue, un encodage des espaces est effectué dans la chaîne de caractère expectedValue: on remplace le code caractère 160 espace&nbsp;par le code caractère 32.&nbsp;

Maintenant cet encodage est egalement effectué pour la chaîne de caractère actualValue (tableValue).
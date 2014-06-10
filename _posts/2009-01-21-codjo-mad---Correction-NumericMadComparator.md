---
layout: post
title: agf-mad - Correction NumericMadComparator
tags: [framework-1-80,codjo-mad]
---
Le ```PreferenceRenderer``` est utilisé pour formater et afficher une donnée (notamment numérique) dans la ```RequestTable```. Pour un format numérique spécifié dans le ```preference.xml```, celui-ci ne prend pas en compte l'attribut ```format```, mais utilise le formateur Java en locale française avec " " (espace) en séparateur de milliers et "." en séparateur de décimales.

Par exemple, le nombre **1234,5** sera affiché dans une cellule de ```RequestTable``` :
```1 234.5```

Le ```NumericMadComparator``` qui est utilisé pour trier les colonnes stipulant un ```sorter="Numeric"``` dans le ```preference.xml``` ne prend pas en compte ce format, mais attend une chaîne de caractères acceptable pour ```Double.valueOf(String)```.

Par exemple, la chaîne **1234.5** sera transformée en nombre correctement.

Le problème est que la chaîne précédemment obtenue par le ```PreferenceRenderer``` ne sera **pas** correctement transformée, et le comparateur considérera que la valeur est ```-Infinity```.

Pour corriger rapidement et avec le minimum d'impact ce problème, nous avons supprimé les espaces dans la chaîne de caractères passée au ```NumericMadComparator```.


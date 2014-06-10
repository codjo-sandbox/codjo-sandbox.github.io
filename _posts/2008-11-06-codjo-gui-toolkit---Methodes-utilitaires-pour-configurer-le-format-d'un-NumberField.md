---
layout: post
title: agf-gui-toolkit - Méthodes utilitaires pour configurer le format d'un NumberField
tags: [framework-1-69,codjo-gui-toolkit]
---
Des méthodes utilitaires ont été déplacées depuis ```GuiUtil``` vers ```NumberField``` pour configurer le format des chiffres affichés par le composant.

* ```
applyDecimalFormat(String decimalFormat, char thousandSeparator, char decimalSeparator)
```
permet de configurer le ```NumberField``` avec le format spécifié (par exemple #,##0.0 permettant de définir un séparateur pour les milliers ainsi qu'un séparateur de décimales au niveau du rendu du composant). Les caractères servant de séparateurs peuvent être customisés.

* ```
applyDecimalFormat(String decimalFormat)
```
permet de configurer le ```NumberField``` avec le format spécifié. Le caractère ' ' (espace) et le '.' sont configurés par défaut.
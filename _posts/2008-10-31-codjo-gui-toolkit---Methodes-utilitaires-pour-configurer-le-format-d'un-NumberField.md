---
layout: post
title: agf-gui-toolkit - Méthodes utilitaires pour configurer le format d'un NumberField
tags: [framework-1-68,codjo-gui-toolkit]
---
Des méthodes utilitaires ont été ajoutées dans ```GuiUtil``` pour configurer et manipuler les formats de chiffres à destination d'un ```NumberField```.
* ```
applyDecimalFormat(NumberField component, String decimalFormat,
                   char thousandSeparator, char decimalSeparator)
```
permet de configurer le ```NumberField``` avec le format spécifié (par exemple #,##0.0 permettant de définir un séparateur pour les milliers ainsi qu'un séparateur de décimales au niveau du rendu du composant). Les caractères servant de séparateurs peuvent être customisés.

* ```
applyDecimalFormat(NumberField component, String decimalFormat)
```
permet de configurer le ```NumberField``` avec le format spécifié. Le caractère ' ' (espace) et le '.' sont configurés par défaut.

* ```
String computeFormatPattern(int decimalLength, DecimalFormatEnum format)
```
permet de calculer un format du type #,##0 en prenant en compte le nombre de décimales passé en paramètre. L'enum permet de spécifier si l'on veut voir les zéros significatifs après la virgule (FULL) ou pas (SIMPLE).
<u>Exemple</u> :
-* ```computeFormatPattern(2, DecimalFormatEnum.FULL)``` donnera #,##0.00. Le rendu de la valeur 1000,50 sera 1 000.50.
-* ```computeFormatPattern(2, DecimalFormatEnum.SIMPLE)``` donnera #,##0.##. Le rendu de la valeur 1000,50 sera 1 000.5.
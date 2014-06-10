---
layout: post
title: agf-test - Enrichissement de la balise click pour gérer le double-click
tags: [codjo-test,framework-1-8]
---
La balise <click> permet de cliquer sur un composant. Il est possible de préciser le nombre de clicks à exécuter sur un composant donné (précisé par un nom). Dans le cas d'une table, il est aussi possible de préciser la ligne (row) ou la cellule (row + column) où l'on souhaite exécuter le click.
&nbsp;
Exemple :

Le code suivant permet de sélectionner la 3e ligne.
```
<click name="maTable" row="2"/>
```\\

Le code suivant permet de double-cliquer sur la première cellule de la table.
```
<click name="maTable" row="0" column="0" count="2"/>
```
---
layout: post
title: agf-test - Gestion des properties dans assertList
tags: [codjo-test,framework-1-25]
---
Ajout de la possibilité d'avoir des properties dans l'expected de la balise 'assertList'.

Dans l'exemple suivant, on teste que la valeur de la 1ere ligne de la combo 'year' est bien égale à l'année dernière :
```
    <tstamp>
    <format property="PREVIOUS_YEAR" pattern="yyyy" locale="fr" offset="-1" unit="year"/>
</tstamp>

...
<assertList name="year" expected="${PREVIOUS_YEAR}" row="0"/>
...
```
---
layout: post
title: agf-release-test - Amélioration de la balise AssertFrame
tags: [framework-1-68,codjo-release-test]
---
Ajout de deux fonctionnalités à la balise ```assertFrame``` :
* Attribut ```matching``` permettant de vérifier partiellement le titre de la frame. Valeurs possibles : ```equals```, ```contains```, ```startsWith```, ```endsWith```, ```regexp```.
Exemple :
```
...
<!-- On recherche la frame dont le titre commence par 'Début du titre' -->
<assertFrame title="Début du titre" matching="startsWith"/>
...
```
* Support des properties. Les properties ```ant``` entourées de ${} sont remplacées par leur valeur (lues du fichier ```test-release.properties```).
Exemple :
```
...
<assertFrame title="SCRIBE ${version} - ${environment}"/>
...
```

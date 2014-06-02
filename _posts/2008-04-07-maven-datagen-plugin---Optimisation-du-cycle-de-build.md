---
layout: post
title: maven-datagen-plugin - Optimisation du cycle de build
tags: [maven-datagen-plugin,framework-1-38,hot-topics]
---
Le cycle de build d'un module datagen a été optimisé. Les optimisations sont : 
* Suppression de la phase ```unjar```
* Suppression de la re-compilation si non nécessaire
* Suppression du packaging si pas de recompile

<u>Exemple de Résultat</u> : Sur le module ```datagen``` de mint.

<table>
<tr>
<th>Opération</th><th>Ancienne version</th><th>Nouvelle Version</th></tr>
<tr>
<td> ```mvn clean install``` </td>
<td> 4 min 50 sec </td>
<td> 4 min 27 sec </td>
</tr>
<tr>
<td> ```mvn install``` (après un ```clean install```) </td>
<td> 1 min </td>
<td> 12 sec </td>
</tr>
</table>

---
layout: post
title: agf-release-test - Ajout de la balise assertTitleBorder
tags: [framework-1-73,codjo-release-test]
---
La balise ```assertTitleBorder``` a été ajoutée. Elle permet de vérifier le titre de la bordure d'un composant.
Les composants supportés sont des ```JComponent``` pour lesquels une bordure de type ```TitleBorder``` est définie.

#### Paramètres

<table>
<tr>
<th>Attribut</th><th>Description</th><th>Obligatoire</th></tr>
<tr>
<td> **name** </td>
<td> Nom du composant ayant une ```TitleBorder```. </td>
<td> oui </td>
</tr>
<tr>
<td> **expected** </td>
<td> Valeur attendue du titre de la bordure. </td>
<td> oui </td>
</tr>
<tr>
<td> **matching** </td>
<td> Permet d'effectuer des comparaisons de type ```contains```, ```startsWith``` ou ```endsWith```, par défaut : ```equals```. </td>
<td> non </td>
</tr>
</table>

#### Exemples

Pour vérifier que le ```JPanel``` ```panelName``` contient bien ```My Title``` :
```
<assertTitleBorder name="panelName" expected="My Title"/>
``
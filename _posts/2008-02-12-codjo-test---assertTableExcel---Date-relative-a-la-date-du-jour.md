---
layout: post
title: agf-test - assertTableExcel - Date relative à la date du jour
tags: [framework-1-31,codjo-test]
---
Il est maintenant possible de définir des dates relatives à la date du jour dans le fichier excel qui sert d'étalon.

Exemple :

<table>
<tr>
<th>Définition</th><th>Texte&nbsp;dans cellule d'un fichier&nbsp;excel</th></tr>
<tr>
<td> date du jour </td>
<td> ${TODAY} </td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x jour </td>
<td> ${TODAY}</u>xD </td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x mois </td>
<td> ${TODAY}</u>xM </td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x ans </td>
<td> ${TODAY}</u>xY </td>
</tr>
<tr>
<td> date du jour&nbsp;-&nbsp;x jour </td>
<td> ${TODAY}-xD </td>
</tr>
</table>
| ... | ... 
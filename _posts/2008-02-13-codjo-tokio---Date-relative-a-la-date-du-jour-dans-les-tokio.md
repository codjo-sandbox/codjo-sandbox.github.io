---
layout: post
title: agf-tokio - Date relative à la date du jour dans les tokio
tags: [framework-1-31,codjo-tokio]
---
Il est maintenant possible de définir des dates relatives à la date du jour dans les fichiers "tokio"

Exemple :
<table>
<tr>
<th>Définition</th><th>Texte dans balise field (pour type Date et Timestamp)</th></tr>
<tr>
<td> date du jour </td>
<td> TODAY </td>
</tr>
<tr>
<td> date du jour <u> x millisecondes  </td>
<td> TODAY</u>x</td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x jour </td>
<td> TODAY</u>xD </td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x mois </td>
<td> TODAY</u>xM </td>
</tr>
<tr>
<td> date du jour <u>&nbsp;x ans </td>
<td> TODAY</u>xY </td>
</tr>
<tr>
<td> date du jour&nbsp;-&nbsp;x jour </td>
<td> TODAY-xD </td>
</tr>
</table>
| ...|...
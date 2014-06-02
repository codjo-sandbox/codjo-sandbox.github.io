---
layout: post
title: maven-agf-plugin - Détermination du prochain numéro de version du Framework
tags: [framework-1-60,maven-codjo-plugin]
---
Prise en compte des release candidate et des patchs dans la détermination du prochain numéro de version du framework.

Exemple :
<table>
<tr>
<th>Dernière version déployée</th><th>Prochaine version</th></tr>
<tr>
<td> 1.25 </td>
<td> 1.26 </td>
</tr>
<tr>
<td> 1.32.1 </td>
<td> 1.33 </td>
</tr>
<tr>
<td> 1.58-rc1 </td>
<td> 1.59 </td>
</tr>
</table>

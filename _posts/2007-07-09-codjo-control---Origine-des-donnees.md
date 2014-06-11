---
layout: post
title: agf-control - Origine des données
tags: [codjo-control,framework-1-4]
---
Les données passant dans un plan d'intégration peuvent avoir plusieur sources:
* agent d'import
* agent de transfert de quarantaine (Q_AP_USER vers Q_AP)
* modification ihm
* autre ???

L'attribut 'step_for' de la balise 'step' du PI a été étendu pour lui permettre de décider si la le control est executé ou non suivant la source de donnée.

Quand les agents se transmettent la requête, il alimentent l'attibut 'chemin' (pathOfRequest) de la requête (ControlJobRequest) par un 'append', ce qui permet à la step de matcher une partie du chemin, et de savoir par ou est passé la demande de control.

**Exemple:** maintenant les données venant de l'import ne sont plus seulement 'batch', mais 'batch/import' est celle venant d'une table de quarantaine ont un chemin égal à 'batch/transferq', ce qui permet à une step ayant l'attribut _step_for = 'batch'_ de prendre les deux source en compte ou si elle vaut _'import'_ de ne s'executer que si les données viennent effectivement de l'agent d'import.

La baslise step a gardée son comportement d'origine, et a été étendue, elle est executé dans les cas suivant &nbsp;
<table>
<tr>
<th>Valeur de l'attribut step_for \</th><th>valeurs possible du chemin contenu dans ControlJobRequest</th></tr>
<tr>
<td> null </td>
<td> * \ </td>
</tr>
<tr>
<td> * </td>
<td> null \ </td>
</tr>
<tr>
<td> all </td>
<td> * \ </td>
</tr>
<tr>
<td> user \ </td>
<td> _user_,&nbsp; _user.add_, _user.update_ \ </td>
</tr>
<tr>
<td> user.add \ </td>
<td> _user_, _user.add_\ </td>
</tr>
<tr>
<td> user.update </td>
<td> _user_, _user.update_ \ </td>
</tr>
<tr>
<td> batch </td>
<td> batch \ </td>
</tr>
<tr>
<td style:color=#ff6600>etapeX \ </td>
<td style:color=#ff6600>etape1/etape2/etape3 </td>
</tr>
<tr>
<td style:color=#ff6600>etape2/etape3 </td>
<td style:color=#ff6600>etape1/etape2/etape3/etape4/etape5</td>
</tr>
</table>
** _\** = n'importe quel valeur._
* _les virgule dénotent différentes possibilitées._\

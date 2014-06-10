---
layout: post
title: maven-delivery-plugin - Possibilité de livrer des fichiers templates pour les modules Batch
tags: [maven-delivery-plugin,framework-1-47]
---
Maintenant il est possible de livrer des fichiers ```\*.template``` dans les modules ```Batch```.

Cela nous permet d'ajouter des variables Delreco dans les scripts Unix et Windows.

Pour pouvoir utiliser cette fonctionnalité, il suffit de nommer les scripts qui contiennent des variables Delreco en ```.template```.

Ex : ```broadcast-internet.bat``` devient ```scribe-broadcast-internet.bat.template```


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
[[Cette modification a été annulée dans le framework v 1.58|http://wp-confluence/confluence/pages/viewpage.action?pageId=6722651]]
</p></td>
          </tr>
</table>


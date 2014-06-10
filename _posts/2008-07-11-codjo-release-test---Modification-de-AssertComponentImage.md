---
layout: post
title: agf-release-test - Modification de AssertComponentImage
tags: [codjo-release-test,framework-1-52,hot-topics]
---
Changement du mode de comparaison d'image :
- On ne fait plus une comparaison de checksum mais une comparaison pixel par pixel
- Plus aucun fichier temporaire n'est créé
- Le format des images étalons est désormais le bmp
\\


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>Il faut regénérer les images étalons pour qu'elles soient au format bmp</p></td>
          </tr>
</table>

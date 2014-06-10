---
layout: post
title: agf-segmentation - Modification of triggers with select from inserted or updated
tags: [framework-1-172-rc2,hot-topics,sybase15-migration,framework-1-172,codjo-segmentation,framework-1-172-rc1]
---
<u>Context</u>:
During [[sybase15-migration]], we have encountered a problem using triggers selecting ```text``` columns from inserted or updated.
To solve the problem, a previous work had been made ([[framework:/2010/10/12/codjo-segmentation - Text columns converted to varchar]]) but it must be roll-backed because of warnings with sybase.

<u>Description</u>:
Previous work has been roll-backed.
Such triggers have been modified in order to not directly select text columns from inserted or updated. Instead, select are made on the table.


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
Do not forget to add in ```livraison-sql.txt```:
* ```TR_PM_CLASSIFICATION_STRUCTURE_I``` and ```TR_PM_CLASSIFICATION_STRUCTURE_U``` creation scripts,
* Segmentation triggers overridden by applications.
</p></td>
          </tr>
</table>

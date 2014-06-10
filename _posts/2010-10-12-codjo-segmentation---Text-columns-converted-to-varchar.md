---
layout: post
title: agf-segmentation - Text columns converted to varchar
tags: [framework-1-170,codjo-segmentation,sybase15-migration,hot-topics]
---
<u>Context</u>:
During [[sybase15-migration]], we have encountered a problem using triggers manipulating ```text``` columns.

<u>Description</u>:
Columns ```PM_EXPRESSION.EXPRESSION``` and ```PM_CLASSIFICATION_STRUCTURE.FORMULA``` are now ```varchar(15000)``` instead of ```text```.


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
Do not forget to add in ```livraison-sql.txt```:
* ```PM_EXPRESSION``` and ```PM_CLASSIFICATION_STRUCTURE``` alter scripts,
* ```sp_SEG_Copy_AxisClassification```, ```sp_SEG_Transcode_Sleeve_Code```, ```sp_SEG_Update_Includes``` and ```sp_SEG_Update_Main_Expression``` creation scripts,
* ```TR_PM_CLASSIFICATION_D```, ```TR_PM_CLASSIFICATION_I```, ```TR_PM_CLASSIFICATION_U```, ```TR_PM_CLASSIFICATION_STRUCTURE_D```, ```TR_PM_CLASSIFICATION_STRUCTURE_I```, ```TR_PM_CLASSIFICATION_STRUCTURE_U``` and ```TR_PM_SEGMENTATION_D``` creation scripts,
* Segmentation triggers and procedures overridden by applications.
</p></td>
          </tr>
</table>

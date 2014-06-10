---
layout: post
title: agf-release-test - Add cell style assertions in the assert-excel step
tags: [framework-1-172,hot-topics,codjo-release-test]
---
<u>Context</u>:
In the Mint application, we export data from UI into excel file and we need to test both content and style of the cells.

<u>Description</u>:
The ```assert-excel``` step has now a new attribute ```matchers``` which contains the list of styles to assert.

<u>Example</u>:
To check only the content, do not set the ```matchers``` attribute:
```xml
<assert-excel expected="expected_file.xls" columnCount="20" rowCount="30"/>
```
To check _bold_, _border_ and _background-color_ styles:
```xml
<assert-excel expected="expected_file.xls" columnCount="20" rowCount="30"
              matchers="border,bold,background-color"/>
```


<table style='background-color: #FFFFCE;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/warning.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>Technically, the excel comparator used for the ```file-assert``` step is now used in the ```assert-excel``` because the style comparator was already written.
Although ```columnCount``` and ```rowCount``` attributes are now deprecated for the comparison, they are still present for backward compatibility.</p></td>
          </tr>
</table>


<u>Documentation</u>:
* [[codjo-release-test - Assertion d'un fichier Excel ouvert en TR|framework:agf-release-test - Assertion d'un fichier Excel ouvert en TR]]
* [[Documentation de référence de la balise assert-excel|framework:assert-excel]]
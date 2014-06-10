---
layout: post
title: agf-test - Ajout de steps web
tags: [framework-1-16,codjo-test]
---
\- AssertCheckBox : asserte la valeur d'une checkbox html
```
<assertCheckBox name="employeeUpdateForm_sensitive" checked="true"/>
```
\- AssertPresent : asserte qu'un élément html identifié par un id est présent ou pas. Par exemple :
```
<assertPresent id="securityEventLink" present="false"/>
```
\- AssertCheckBox en dehors d'un formulaire web.

\- ClickCheckBox en dehors d'un formulaire web.&nbsp;
---
layout: post
title: agf-tokio - Chargement des fichiers avec le nouveau formalisme
tags: [kaizen-tr,framework-1-101,codjo-tokio,hot-topics]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Il est maintenant possible de charger les fichiers tokio avec le formalisme "allégé".

**NB** : Pour prendre en compte cette modification, la validation par les dtd a été désactivée.

<u>Exemple :</u> {section}
{column:width=50%}
Avant :
```
<table name="AP_TABLE" orderClause="FIELD_1">
 <row>
   <field name="FIELD_1" value="value1"/>
   <field name="FIELD_2"/> // valeur null
 </row>
</table>

<table name="AP_EMPTY_TABLE"> // table vide
```
{column}

{column:width=50%}
Après :
```
<AP_TABLE orderClause="FIELD_1">
  <row>
    <FIELD_1 value="value1"/>
    <FIELD_2/> // valeur null
  </row>
</AP_TABLE>

<AP_EMPTY_TABLE/> // table vide
```
{column}
{section}


---
layout: post
title: agf-tokio - Correction de la gestion des données partagées
tags: [framework-1-106,codjo-tokio]
---
L'unicité des ```required``` ne fonctionnait pas dans le cas suivant:

{section}
{column}
```title=entity
<entity id="MyEntity">
  <required>
    <TABLE2>
      <row>
        <FIELD1 value="value1"/>
        <FIELD2 value="value2"/>
      </row>
    </TABLE2>
  </required>
</entity>
```
{column}
{column}
```title=tokio
<create-entity name="MyEntity"/>

<TABLE2>
  <row>
    <FIELD1 value="value1"/>
    <FIELD2 value="value2"/>
  </row>
</TABLE2>
```
{column}
{section}
La ligne dans la table2 du required de l'entité était insérée alors qu'elle ne le devait pas.
Cette erreur a été corrigée.
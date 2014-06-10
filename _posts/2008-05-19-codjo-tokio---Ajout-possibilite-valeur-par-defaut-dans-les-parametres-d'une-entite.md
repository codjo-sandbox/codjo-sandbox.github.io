---
layout: post
title: agf-tokio - Ajout possibilité valeur par défaut dans les paramètres d'une entité
tags: [codjo-tokio,framework-1-45]
---
Il est désormais possible de spécifier des valeur par défaut pour des paramètres d'entité. Les paramètres définis avec des valeurs par défaut peuvent être omises lors de l'instanciation de l'entité.
```
// définition de l'entité
  <entity id="Entity">
    <parameters>
      <parameter name="param1" default="defaultParam1"/>
    </parameters>
    <body>
      <table name="MY_TABLE">
        <row id="rowId">
          <field name="FIELD1" value="field1"/>
          <field name="FIELD2" value="@param1@"/>
        </row>
      </table>
    </body>
  </entity>
```
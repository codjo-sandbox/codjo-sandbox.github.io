---
layout: post
title: maven-datagen-plugin - Compatibilité des fields ancien formalisme dans le XSD
tags: [framework-1-105,maven-datagen-plugin,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}
Le XSD a été modifié afin de rendre possible l'utilisation de "field" ancien formalisme dans une "row" nouveau formalisme.

<u>Exemple</u> :
```
<AP_TABLE>
  <row>
    <FIELD1 value="3"/>
    <field name="field2" value="titi"/>
    <FIELD3 value="toto"/>
  </row>
</AP_TABLE>
```
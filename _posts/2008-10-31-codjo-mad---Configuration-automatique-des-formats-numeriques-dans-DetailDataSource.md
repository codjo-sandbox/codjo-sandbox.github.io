---
layout: post
title: agf-mad - Configuration automatique des formats numériques dans DetailDataSource
tags: [framework-1-68,codjo-mad]
---
Lors de la déclaration d'un composant graphique sur un ```DetailDataSource```, la définition du type de champ dans datagen est prise en compte automatiquement pour configurer le renderer sur les ```NumberField```.

**{<u>}Exemples{</u>}** :
* ```<field label="Sensi" name="sensi" sql="SENSI" sql-type="numeric" sql-precision="5,3"/>```
appliquera le format #,##0.000 sur le composant ```NumberField```.
* ```xml
<field label="Bnp" name="bnp" sql="BNP" sql-type="numeric" sql-precision="5,0"/>```
appliquera le format #,##0 sur les composants ```NumberField```.
---
layout: post
title: agf-datagen - Modification de la balise handler-select
tags: [codjo-datagen,framework-1-51]
---
La valeur par défaut permettant d'indiquer le type de la requête de sélection est maintenant positionnée par défaut sur ```SQL``` à la place de ```OQL```.

Donc maintenant:
```xml
<handler-select id="selectHierAffectByDate">
    <query>{call sp_smartHierAffect_select(@SEARCH_DATE  = ?)} </query>
    <arg type="java.sql.Date">searchDate</arg>
</handler-select>
```
est équivalent à l'ancienne écriture :
```xml
<handler-select id="selectHierAffectByDate">
    <query type="SQL">{call sp_smartHierAffect_select(@SEARCH_DATE  = ?)} </query>
    <arg type="java.sql.Date">searchDate</arg>
</handler-select>
```

**NB** : Cette écriture est beaucoup plus condensée qu'un ```handler-sql``` pouvant ramener toutes les colonnes de la table.
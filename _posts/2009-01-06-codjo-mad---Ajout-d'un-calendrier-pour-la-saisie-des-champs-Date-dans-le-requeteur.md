---
layout: post
title: agf-mad - Ajout d'un calendrier pour la saisie des champs Date dans le requeteur
tags: [framework-1-78,codjo-mad]
---
Modification de la classe ```SqlRequetor``` afin d'ajouter un mécanisme détectant les champs date et affichant, dans ce cas, un calendrier facilitant la saisie.

Cette fonctionnalité nécessite de spécifier un type ```Date``` (et non pas ```Timestamp```) dans la configuration _datagen_


```
     <field name="holdDate" type="java.sql.Date">
           <description>Date</description>
           <!--<sql type="timestamp"/>-->
           <sql type="date"/>
      </field>
```
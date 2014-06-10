---
layout: post
title: agf-datagen - Gestion des modèles de BD non standards
tags: [framework-1-114,codjo-datagen,maven-datagen-plugin]
---
Ajout du mode "```legacy```" pour pouvoir gérer les bases de données ne respectant pas les normes de la plateforme de développement JAVA. 

{info:title=Développement exploratoire}
Ce mode a été mis en place afin de pouvoir profiter du Kaizen TR sur les applications hors datagen. Actuellement utilisé sur GPStar, il a vocation à l'être également sur Benchmark. 
{info}

Ce mode a deux effets : 
1. Les noms des colonnes correspondent directement aux noms java
_Exemple_ : 
```xml
...
<field name="subGroup" type="varchar">
  <sql type="varchar" required="true" precision="50"/>
</field>
...
``` 
Dans ce cas la colonne du champs ```subGroup``` sera en BD:
-> cas standard : ```SUB_GROUP```.
-> cas legacy : ```subGroup```.
1. La limite de taille des noms de colonnes et de tables n'est plus vérifiée (limite fixée à 28 caractères en standard)

<u>Exemple</u> : Pour activer le mode il faut positionner la propriété ```com.agf.datagen.legacyMode``` à ```true```.
```
mvn datagen:generate-tokio-xsds -Dcom.agf.datagen.legacyMode=true
```
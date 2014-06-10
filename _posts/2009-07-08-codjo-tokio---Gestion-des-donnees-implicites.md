---
layout: post
title: agf-tokio - Gestion des données implicites
tags: [kaizen-tr,framework-1-103,codjo-tokio,hot-topics]
---
{info:title=Dans le cadre du Kaizen TR}{info}

L'attribut ```autoComplete``` a été mis en place dans les balises ```row```, ```copy``` et ```replace```.
Il permet de générer automatiquement des valeurs :

* pour les ```fields``` non renseignés.
* pour les clés étrangères : Cf. [[doc|codjo-tokio - Résolution des clés étrangères]]

<u>Exemple</u>
```xml
<AP_TEST>
    <row autoComplete="true">
        <COL_A/>
        <COL_B value="MY_VALUE"/>
        <!-- Les autres colonnes seront renseignées automatiquement. -->
        <!-- Les tables liées seront remplies automatiquement si nécessaire, y compris -->
        <!-- sur plusieurs niveaux. -->
    </row>
    <row>
        <COL_A value="MY_SECOND_VALUE"/>
    </row>
</AP_TEST>
```

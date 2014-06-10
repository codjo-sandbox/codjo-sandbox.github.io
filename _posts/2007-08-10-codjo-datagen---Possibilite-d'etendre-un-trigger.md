---
layout: post
title: agf-datagen - Possibilité d'étendre un trigger
tags: [framework-1-9,codjo-datagen]
---
Il devient possible d'étendre un trigger à l'aide des balises append-to-trigger-delete, append-to-trigger-insert et append-to-trigger-update (par exemple étendre dans une application un trigger défini dans une librairie).

Ceci est nécéssaire dans la mesure où Sybase n'autorise qu'un trigger delete, insert et update par table.

Exemple :
Déclaration du trigger :
```
<entity name="com.agf.segmentation.server.data.Classification"
        table="PM_CLASSIFICATION">
    ...
    <trigger-delete>
        <sql>
            Code SQL du trigger
        </sql>
    </trigger-delete>
    ...
</entity>
```

Extension du trigger :
```
<append-to-trigger-delete
       name="com.agf.segmentation.server.data.Classification">
    <sql>
        Code SQL supplémentaire
    </sql>
</append-to-trigger-delete>
```

Le trigger final sera la concaténation du trigger de départ puis de l'extension du trigger.

Comme les éléments add-field ou add-handler, ces balises doivent être au niveau de l'élément /data du fichier datagen.
---
layout: post
title: agf-datagen - Possibilité d'ajouter un handler-sql à une entity
tags: [framework-1-8,codjo-datagen]
---
Il est dorénavant possible d'ajouter un handler sql à une entity de la même façon que pour ajouter un champ. Exemple :

```xml
    <add-handler-sql to="com.agf.segmentation.server.data.Classification">
        <handler-sql id="selectClassificationWithReInvoice" return-pk="false">
            <attributes>
                <name>classificationId</name>
            </attributes>
            <query>
                select CLASSIFICATION_ID
                from PM_CLASSIFICATION
                where CLASSIFICATION_ID != ?
                and RE_INVOICE = 1
            </query>
            <arg>classificationId</arg>
        </handler-sql>
    </add-handler-sql>
```
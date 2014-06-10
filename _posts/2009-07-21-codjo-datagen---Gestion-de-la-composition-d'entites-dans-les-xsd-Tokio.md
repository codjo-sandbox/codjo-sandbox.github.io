---
layout: post
title: agf-datagen - Gestion de la composition d'entités dans les xsd Tokio
tags: [framework-1-105,codjo-datagen,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Les balises ```include-entities``` et ```create-entity``` peuvent désormais être utilisées dans un fichier ```entities```.

<u>Exemple</u> :
```xml
<entities>
    <include-entities file="referential.entities"/>

    <entitiy>
        <body>
            <create-entity name="currency"/>
        </body>
    </entitiy>
</entities>
```
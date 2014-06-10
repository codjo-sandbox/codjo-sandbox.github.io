---
layout: post
title: agf-tokio - Composition d'entités
tags: [framework-1-105,codjo-tokio,hot-topics,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Il est maintenant possible de créer des entités à l'intérieur d'autres entités.

<u>Exemple</u> :
```xml|title=parents.entities
<entities>
    <include-entities file="childs.entities"/>
    <entity id="father">
        <body>
            <create-entity name="son">
                <parameter name="age" value="12"/>
            </create-entity>
            ...
        </body>
    </entity>
</entities>
```

```xml|title=childs.entities
<entities>
    <entity id="son">
        <parameters>
            <parameter name="age"/>
        </parameters>
        <body>
            ...
        </body>
    </entity>
</entities>
```
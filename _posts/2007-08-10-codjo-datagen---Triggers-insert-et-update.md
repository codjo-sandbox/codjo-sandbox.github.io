---
layout: post
title: agf-datagen - Triggers insert et update
tags: [framework-1-9,codjo-datagen]
---
On peut maintenant créer des triggers d'insert et d'update avec datagen, à l'aide des balises <trigger-insert> et <trigger-update>. Exemple :

```
<entity name="...">
    <features>
        <trigger-insert>
            <sql>
                -- Code du trigger
            </sql>
        </trigger-insert>
        ...
    </features>
    ...
</entity>
```

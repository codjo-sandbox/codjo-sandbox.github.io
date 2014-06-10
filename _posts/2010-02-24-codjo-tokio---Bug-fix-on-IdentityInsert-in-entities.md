---
layout: post
title: agf-tokio - Bug fix on IdentityInsert in entities
tags: [framework-1-136,codjo-tokio]
---
<u>Context</u>:
In an entity definition file, the ```required``` scope doesn't take into account the ```identityInsert``` attribute.

<u>Description</u>:
The bug has been fixed.

<u>Example</u>:
In the following case, "TABLE2" has an ```identityInsert``` attribute
```
<entities>
    <entity id="MyEntityIdentityInsert">
        <comment>MyEntity</comment>
        <parameters>
            <parameter name="param1"/>
            <parameter name="param2"/>
        </parameters>
        <body>
            <TABLE1 orderClause="FIELD1">
                <row>
                    <FIELD1 value="field4"/>
                </row>
            </TABLE1>

        </body>
        <required>
            <TABLE2 identityInsert="true">
                <row>
                    <FIELD1 value="@param1@"/>
                    <FIELD2 value="@param2@"/>
                </row>
            </TABLE2>
        </required>

    </entity>
</entities>
```
see [[framework:Utilisation de codjo-tokio]]

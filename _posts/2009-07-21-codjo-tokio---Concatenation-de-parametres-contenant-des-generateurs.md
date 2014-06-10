---
layout: post
title: agf-tokio - Concaténation de paramètres contenant des générateurs
tags: [framework-1-105,codjo-tokio,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Il est maintenant possible de concaténer des paramètres d'entités contenant des générateurs.

<u>Exemple</u> :
```xml
<entity id="somebody">
    <parameters>
        <parameter name="firstName">
            <generateString precision="32"/>
        </parameter>
        <parameter name="lastName">
            <generateString precision="32"/>
        </parameter>
        <parameter name="fullName" value="@firstName@ @lastName@"/>
    </parameters>

    <body>
        <CUSTOMER>
            <row>
                <FULL_NAME value="@fullName@"/>
                <FULL_NAME_BIS value="M. @lastName@ @firstName@"/>
            </row>
        </CUSTOMER>
    </body>
</entity>
```
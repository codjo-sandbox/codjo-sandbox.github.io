---
layout: post
title: agf-tokio - Ajout possibilité valeur par défaut dans les paramètres d'une entité
tags: [framework-1-45,codjo-tokio,hot-topics]
---
Evolution de la fonctionnalité de paramétrage par défaut des entités.


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>Il est possible que cette évolution nécessite une mise à jour des tests release utilisant des entités.
</p></td>
          </tr>
</table>


Désormais si un paramètre d'entité n'a pas de valeur par défaut définie et n'est pas spécifiée lors de la création d'entité, alors le test échoue en levant une ```TokioLoaderException```.

De plus, il est désormais possible d'affecter une valeur par défaut nulle à un paramètre.

Exemple :
```
<entity id="EntityWithDefaultValues">
        <parameters>
            <parameter name="paramDefaultEmptyString" default=""/>
            <parameter name="paramDefaultNull" default="null"/>
        </parameters>
        <body>
            <table name="MY_TABLE">
                <row>
                    <field name="FIELD_DEFAULT_EMPTY_STRING" value="@paramDefaultEmptyString@"/>
                    <field name="FIELD_DEFAULT_NULL" value="@paramDefaultNull@"/>
                </row>
            </table>
        </body>
</entity>
```
Avec cette syntaxe, la chaîne de caractères "null" est remplacée par la valeur nulle, lors de l'insertion en base.\\


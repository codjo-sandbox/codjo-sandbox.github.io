---
layout: post
title: agf-test, agf-tokio - Ajout de possibilité d'utiliser des varaiables ANT dans un fichier tokio
tags: [framework-1-16,codjo-test,codjo-tokio]
---
Il est désormais possible d'utiliser les variables Ant et les&nbsp;variables spécifiées dans le fichier ```test-release.config```&nbsp;lors de l'écriture d'un fichier tokio.

La syntaxe utilisée est la suivante :
```
<Scenarii name="AUTOMATIC">
    <Scenario id="configTest">
        <input>
            <table name="CONFIG">
                <row id="myConfig">
                    <field name="HOST" value="${testEnvironment.host}"/>
                    <field name="PORT" value="${testEnvironment.port}"/>
                    <field name="BASE_DIR" value="${basedir}"/>
                </row>
            </table>
        </input>
        <etalon>
            <table name="CONFIG">
                <row inheritId="myConfig">
                    <field name="UPDATED_BY" value="${testEnvironment.user}"/>
                </row>
            </table>
        </etalon>
    </Scenario>
</Scenarii>
```
Les variables définies entre **${** et&nbsp; **}**&nbsp;seront automatiquement remplacées par leurs valeurs respectives avant le chargement en base du fichier tokio.

Il devient donc possible par exemple, de tester les champs de type "UPDATED_BY" qui se remplissent automatiquement avec le nom de l'utilisateur loggué sur l'application&nbsp;lors des tests de gestion des droits.
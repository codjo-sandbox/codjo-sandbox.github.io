---
layout: post
title: agf-tokio - Possibilité de définir les propriétés système d'exécution
tags: [codjo-tokio,framework-1-9]
---
Il est dorénavant possible d'ajouter une balise property ou une balise properties dans un fichier tokio de façon à définir les propriétés système d'exécution. Exemples :
```
<Scenarii name="Changement de properties">
    <Scenario>
        <properties filename="properties/overwrite.properties" overwrite="true"/>
        <property name="user.name" value="toto"/>
        <input/>
        <etalon/>
    </Scenario>
</Scenarii>
```
ou bien
```
<story id="Changement de properties">
    <properties filename="../properties/load.properties" overwrite="true"/>
    <property name="user.name" value="toto"/>
    <input/>
</story>
```
ou encore
```
<cases>
    <case id="Changement de properties">
        <properties filename="../properties/load.properties" overwrite="true"/>
        <property name="tralala" value="youpi"/>
        <input/>
        <output/>
    </case>
</cases>
```
```<properties>``` charge un fichier de propriétés spécifié en paramêtres. L'option ```overwrite``` permet de spécifier si l'ensemble des paramêtres sont remplacés y compris ceux qui ne sont pas spécifiés dans le fichier.

```<property>```&nbsp;permet de remplacer un unique paramêtre.

Les balises sont cumulables et prises en compte dans l'ordre de spécification.
\\
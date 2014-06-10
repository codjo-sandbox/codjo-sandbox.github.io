---
layout: post
title: agf-control - Ajout des filtres BD
tags: [codjo-control,framework-1-8]
---
Maintenant on peut utiliser des filtres BD à la place des filtres d'affichage classiques dans les quarantaines.

Il suffit de configurer l'application qui se nourrit des filtres de la façon suivante :

1. Dans le quarantine.xml préciser les champs à filtrer en mode base des données
```
<window title="Quarantaine de la comptabilité générale">
<preference>QUserDecisivEntryWindow</preference>
  <dbFilter>errorType</dbFilter>
  <dbFilter>sourceFile</dbFilter>
</window>
```
2. Dans le fichier préference.xml, renomer le handler dans la balise <selectAll> **selectAllXXX** en **selectAllXXXWithParameters**

3. Ajouter les droits pour les handler suivants :
```
<include>selectAllQUserTimeSheetWithParameters</include>
<include>selectAllQuarantine*</include>
```
4. Vérifier que le module datagen a une dependence vers control
```
    <packaging>pom</packaging>
    <build>
        <plugins>
            <plugin>
                <groupId>com.agf.maven.mojo</groupId>
                <artifactId>maven-datagen-plugin</artifactId>
                <configuration>
                    <includes>
                    	<include>
				<groupId>com.agf.control</groupId>
			    	<artifactId>codjo-control-server</artifactId>
			    	<classifier>datagen</classifier>
		    	</include>
```
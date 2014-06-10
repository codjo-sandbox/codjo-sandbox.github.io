---
layout: post
title: agf-release-test - Ajout d'une balise de nettoyage de répertoire
tags: [framework-1-78,codjo-release-test]
---
Une nouvelle balise ```cleanup``` permettant de nettoyer un répertoire local ou distant a été ajoutée.
Elle prend un attribut ```dir``` indiquant une clé pour laquelle les propriétés local et remote seront définies dans le fichier test-release.config.

Exemple :
```
<cleanup dir="tempDir"/>
```

Contenu du fichier test-release.config :
```
tempDir.local = ${project.basedir}/target/release-test/tmp
tempDir.remote = ${unixApplicationDirectory}/DAT1/OUT
```

Doc : http://wp-confluence/confluence/display/framework/cleanup
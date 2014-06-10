---
layout: post
title: agf-release-test - Copie de fichier dans un répertoire applicatif
tags: [framework-1-78,codjo-release-test]
---
Ajout du paramètre ```in``` à la balise ```copy-to-inbox``` afin de pouvoir copier un fichier dans un répertoire spécifique autre que la ```INBOX```.
Ce paramètre prend comme valeur une clé pour laquelle les propriétés local et remote seront définies dans le fichier ```test-release.config```

Exemple de copie avec chemin et le contenu du fichier ```test-release.config``` :
```xml
<copy-to-inbox file="RTG_EM.txt" in="inputDir"/>
```
```
inputDir.remote = ${unixApplicationDirectory}/DAT1/OUT
inputDir.local = ${project.basedir}/target/release-test/tmp
```

cf doc : http://wp-confluence/confluence/display/framework/copy-to-inbox

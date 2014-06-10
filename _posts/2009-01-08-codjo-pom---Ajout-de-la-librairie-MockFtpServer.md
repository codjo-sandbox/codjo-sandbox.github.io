---
layout: post
title: agf-pom - Ajout de la librairie MockFtpServer
tags: [framework-1-78,codjo-pom,hot-topics]
---
La librairie MockFtpServer a été ajoutée au super-pom.
Elle permet de simuler un serveur FTP.

Pour l'utiliser, ajouter ceci dans votre fichier pom.xml :
```
<dependency>
    <groupId>org.mockftpserver</groupId>
    <artifactId>MockFtpServer</artifactId>
</dependency>
```

(cf. [[MockFtpServer|swdev:MockFtpServer]])
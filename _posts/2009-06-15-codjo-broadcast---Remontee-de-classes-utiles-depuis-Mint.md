---
layout: post
title: agf-broadcast - Remontée de classes utiles depuis Mint
tags: [framework-1-100,codjo-broadcast]
---
<u>codjo-broadcast-common (scope test)</u>

Ajout des classes _ComputedFieldTestCase_ et _PreferenceMock_ pour tester les _ComputedField_

<u>codjo-broadcast-server</u>

Ajout de la classe _AbstractSqlResourceComputedField_ qui s'appuie sur un code sql externalisé dans un fichier au lieu d'un appel JDBC. Le fichier en question doit être localisé dans le même package et doit porter le même nom que le _ComputedField_ implémenté.

<u>Exemple</u> :
```
main/java/com/agf/toto/server/broadcast/MyComputedField.java
main/resources/com/agf/toto/server/broadcast/MyComputedField.sql
```
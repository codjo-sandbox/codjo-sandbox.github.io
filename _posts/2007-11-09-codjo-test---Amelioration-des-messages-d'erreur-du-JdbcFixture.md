---
layout: post
title: agf-test - Amélioration des messages d'erreur du JdbcFixture
tags: [framework-1-19,codjo-test]
---
Les messages d'erreur sur les assert d'objet SQL ont été améliorés.

<u>Exemple</u> : L'assertion
```java
jdbc.assertTableExists("AP_BAD_NAME");
```
renverra l'erreur suivante : ```Table 'AP_BAD_NAME' exists expected:<true> but was:<false>```
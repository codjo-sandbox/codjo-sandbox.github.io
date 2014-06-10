---
layout: post
title: agf-security - Correction bug driver Sybase
tags: [codjo-security,framework-1-13]
---
Le bug portant sur des modèles de sécurité volumineux (> 17ko) a été résolu.

La méthode de résolution est :

```java
String xml = XmlCodec.toXml(manager);
statement.setAsciiStream(3, new ByteArrayInputStream(xml.getBytes()), xml.length());
```

**ATTENTION** : En conséquence, le modèle ne doit pas comporter de caractère hors ASCII.


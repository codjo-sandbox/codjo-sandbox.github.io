---
layout: post
title: agf-test - Ajout de la classe ResultSetMock
tags: [codjo-test,framework-1-26]
---
Ajout de la classe ```ResultSetMock``` implémentant l'interface ```java.sql.ResultSet```. Avec Ajout de méthode sur la classe ```StatementMock``` pour en tenire compte.

<u>Exemple</u>
```java
connectionMock.mockCreateStatement(new StatementMock(log).mockResultSet(new ResultSetMock()));
```

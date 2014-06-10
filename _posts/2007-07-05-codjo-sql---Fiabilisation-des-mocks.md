---
layout: post
title: agf-sql - Fiabilisation des mocks
tags: [codjo-sql,framework-1-4]
---
Dans la classe **```JdbcServiceUtilMock```**. Amélioration de la stabilité pour le ```LogString``` dans le cas null.

Le code suivant ne lance plus un ```NullPointerException```

```java
new JdbcServiceUtilMock().getConnectionPool(null, null);
```


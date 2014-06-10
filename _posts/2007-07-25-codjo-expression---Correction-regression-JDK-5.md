---
layout: post
title: agf-expression - Correction regression JDK 5
tags: [framework-1-7,codjo-expression]
---
Avec le JDK 5, il n'est plus possible de comparer des ```Timestamp``` avec des ```Date```.

Le code suivant génère un ```ClassCastException``` :

```java
Date date = Date.valueOf("2004-10-10");
java.sql.Timestamp  timestamp = Timestamp.valueOf("2004-01-01 10:00:00.0");
timestamp.compareTo(date);
```

Pour corriger le problème, l'```ExpressionManager``` converti les ```Timestamp``` en ```Date```.

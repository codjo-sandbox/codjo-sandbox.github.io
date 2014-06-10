---
layout: post
title: agf-test - Possibilité de mocker prepared et callable statements
tags: [framework-1-115,codjo-test]
---
La classe ```ConnectionMock``` permettait de renvoyer un ```Statement``` par la méthode ```createStatement()``` si un appel à ```mockCreateStatement(Statement)``` avait été fait avant. Ce mécanisme mock est désormais mis en place pour les ```PreparedStatement``` et les ```CallableStatement``` par des appels aux méthodes ```prepareStatement(...)``` et ```prepareCall(...)``` respectivement.

Le passage du statement mocké se fait toujours par ```mockCreateStatement(Statement)```.

Par exemple :
```
PreparedStatementMock stm = new PreparedStatementMock();
ConnectionMock cnx = new ConnectionMock();
cnx.mockCreateStatement(stm);
[[...]]
```

De plus les classes ```PreparedStatementMock``` et ```CallableStatementMock``` ont également été créées.
---
layout: post
title: agf-sql - Ajout d'operations sur le plugin
tags: [codjo-sql,framework-1-13]
---
Il est maintenant possible via le plugin ```JdbcServerPlugin``` d'avoir les operations permettant de manipuler les pools de connexions.

<u>Exemple :</u>

```java
JdbcServerPlugin plugin = ....

plugin.getOperations().createPool(myId, databaseLogin, databasePassword);

ConnectionPool pool = plugin.getOperations().getPool(myId);
... utilisation du pool ...

plugin.getOperations().destroyPool(myId);
```

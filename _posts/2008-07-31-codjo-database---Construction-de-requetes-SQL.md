---
layout: post
title: agf-database - Construction de requêtes SQL
tags: [framework-1-55,codjo-database]
---
```DatabaseQueryHelper``` a été créé dans ```codjo-database```.
Cette classe permet de construire des requêtes SQL selon les spécificités des différentes bases utilisées.
Les requêtes suivantes sont actuellement supportées :
* ```select```
* ```create table```
* ```insert```
* ```update```
* ```create index```
* ```alter table add column```


<u>Exemple</u> : ```select COL_A, COL_B from #MY_TABLE``` (en Sybase)
```java
DatabaseQueryHelper databaseQueryHelper = databaseFactory.createDatabaseQueryHelper();
String select = databaseQueryHelper
   .buildSelectQuery(new SqlTable("MY_TABLE", true), "COL_A", "COL_B");
```


<u>Exemple</u> : ```select * from #MY_TABLE``` (en Sybase)
```java
DatabaseQueryHelper databaseQueryHelper = databaseFactory.createDatabaseQueryHelper();
String select = databaseQueryHelper
   .buildSelectQuery(new SqlTable("MY_TABLE", true), true);
```


<u>Exemple</u> : ```update MY_TABLE set COL_A="something"``` (en Sybase)
```java
DatabaseQueryHelper databaseQueryHelper = databaseFactory.createDatabaseQueryHelper();
String select = databaseQueryHelper
   .buildUpdateQuery(new SqlTable("MY_TABLE"), new SqlField("COL_A", "something");
```


<u>Exemple</u> : ```insert into MY_TABLE ( COL_A ) values ( ? )``` (en Sybase)
```java
DatabaseQueryHelper databaseQueryHelper = databaseFactory.createDatabaseQueryHelper();
String select = databaseQueryHelper
   .buildInsertQuery(new SqlTable("MY_TABLE"), new SqlField("COL_A");
```
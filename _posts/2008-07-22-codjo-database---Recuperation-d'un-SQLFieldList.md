---
layout: post
title: agf-database - Récupération d'un SQLFieldList
tags: [framework-1-53,codjo-database,hot-topics]
---
La création de SQLFieldList a changé. Maintenant, il faut passer par la classe ```DatabaseFactory``` se trouvant dans ```codjo-database```.

<u>Exemple</u> :
```java
public class MyClass {
   private DatabaseFactory databaseFactory = new DatabaseFactory();
   
   public SQLFieldList getSQLFieldList(...) {
      return databaseFactory.createSQLFieldList(...);
   }
}
```
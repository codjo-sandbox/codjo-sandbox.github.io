---
layout: post
title: agf-mad - Possibilité d'ajouter un Handler SQL par code
tags: [framework-1-66,codjo-mad]
---
Il est maintenant possible d'ajouter par code un ```handler-sql```.

<u>Exemple</u>
* Définition du handler SQL
```java
public class MySelectHandler extends AbstractSqlHandler {
    public MySelectHandler(DatabaseQueryHelper queryHelper) {
        super(new String[[]]{"myId"}, "select ...", queryHelper);
    }

    @Override
    protected String buildQuery(Map<String, String> arguments) {
        ...
        return ...;
    }


    @Override
    protected void fillQuery(PreparedQuery query, Map<String, String> arguments) {
        query.setString(1, arguments.get("value") );
        ...
    }
}

```
* Déclaration au niveau du plugin mad
```java
madServerPlugin.getConfiguration().addHandlerSql(MySelectHandler.class);
```

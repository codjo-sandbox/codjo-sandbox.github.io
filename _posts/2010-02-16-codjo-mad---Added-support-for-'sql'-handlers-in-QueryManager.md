---
layout: post
title: agf-mad - Added support for 'sql' handlers in QueryManager
tags: [framework-1-134,codjo-mad]
---
<u>Context:</u>
An aspect can access some details of the request that triggered it by calling the ```QueryManager.getQuery(String)``` method. This method throws an ```IllegalArgumentException``` if the handler's call was not present in the current request, or if that handler's xml request fragment is not supported by the ```QueryManager```'s implementation.

<u>Description:</u>
When using an aspect on a SQL handler, one could not retrieve the ```Query``` objects of the request because the ```QueryManager``` threw the exception:
```java.lang.IllegalArgumentException: Le type de handler 'handler-sql' est inconnu !```

Now the ```QueryManager``` implementation handles queries of ```handler-sql``` type.

<u>Example:</u>
Considering the following _datagen_ handler:
```xml
<handler-sql id="changeAmount">
    <query><![CDATA[
    UPDATE myTable 
    SET amount = ?,
        updateBy = ?,
        updateDatetime = getdate()
    WHERE id = ?
    ]]></query>
    <arg>amount</arg>
    <arg>user</arg>
    <arg>id</arg>
</handler-sql>
```

And the following aspect's join-points definition:
```xml
<aspect id="changeAmountAspectId" class="com.agf.foo.ChangeAmountAspect">
    <join-points>
        <join-point call="before" point="handler.execute" argument="changeAmount"/>
    </join-points>
</aspect>
```

The handler's query arguments can be accessed like this:
```title=ChangeAmountAspect.java
protected void doRun(AspectContext context) throws AspectException {
    QueryManager manager = (QueryManager)context.get(QueryManager.class.getName());
    Query[[]] queries = manager.getQuery("changeAmount");
    Map map = queries[[0]].rowToMap();

    int amount = Integer.parseInt((String)map.get("amount"));
    String user = (String)map.get("user");
    <etc.>
}
```
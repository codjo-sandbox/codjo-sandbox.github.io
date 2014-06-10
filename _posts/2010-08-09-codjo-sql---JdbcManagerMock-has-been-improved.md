---
layout: post
title: agf-sql - JdbcManagerMock has been improved
tags: [framework-1-159,codjo-sql]
---
<u>Context</u>:
For [[framework:/2010/08/09/codjo-security - SecurityServerPlugin is no more dependent on JdbcServerPlugin]] testing purpose, it was needed to improve ```JdbcManagerMock```.

<u>Description</u>:
```JdbcManagerMock``` existing methods have been improved.
Before, ```JdbcManagerMock.getPool(...)``` returned ```null```, now it returns any ```ConnectionPool``` previously created by ```JdbcManagerMock.createPool(...)```.

```java
UserId userId = UserId.createId("tata", "yoyo");
JdbcManagerMock jdbcManagerMock = new JdbcManagerMock();

assertNull(jdbcManagerMock.getPool(userId);

ConnectionPool connectionPool = jdbcManagerMock .createPool(userId, "tata", "yoyo");

assertNotNull(connectionPool);
asserEquals(connectionPool, jdbcManagerMock.getPool(userId));
```

see: [[framework:codjo-sql]]
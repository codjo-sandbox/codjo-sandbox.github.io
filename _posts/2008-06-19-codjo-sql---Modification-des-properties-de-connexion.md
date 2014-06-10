---
layout: post
title: agf-sql - Modification des properties de connexion
tags: [codjo-sql,framework-1-49]
---
Les clefs ```USER``` et ```PASSWORD``` ont été changées en minuscule afin de supporter ORACLE et SYBASE. Les constantes liées ont été mises à jour.

```java
public class ConnectionPoolConfiguration implements Cloneable {
    static final String USER_KEY = "user";
    static final String PASSWORD_KEY = "password";
    ...
``` 
---
layout: post
title: agf-mad - HandlerCommand amélioration du toBean
tags: [framework-1-7,codjo-mad]
---
Dans les ```HandlerCommand``` et la méthode ```toBean()``` du ```CommandQuery``` il est maintenant possible de choisir les attributs qui seront positionné.

Par exemple, si on ne veut pas que le ```securityId``` soit  ```setter``` : 

```java
public CommandResult executeQuery(CommandQuery query) throws HandlerException {
    Security security = new Security();
    query.toBean(security, new PropertyFilter() {
        public boolean acceptValue(String propertyName, String value) {
            return !"securityId".equals(propertyName);
        }
    });
    ...
```

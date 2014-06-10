---
layout: post
title: agf-mad - Associate an HandlerMap with a user session
tags: [framework-1-123,codjo-mad]
---
<u>Context</u>:

For the DAMAS software, we need to associate an ```HandlerMap``` to the user session. The goal is to provide a mechanism to rebuild at runtime the user handlers.

<u>Description</u>:

In the ```HandlerMapBuilder``` we add the ```UserId``` to the signature of ```createHandlerMap(...)```.

<u>Example</u>:

```java
HandlerMap handlerMap = 
     handlerMapBuilder.createHandlerMap(userId, new Object[[]]{userId, pool, ..});
```

see: [[codjo-mad - Handler construction principle]]
---
layout: post
title: agf-mad - Handler creation can be customized
tags: [framework-1-120,codjo-mad]
---
<u>Context</u>:
For the ```DAMAS``` software we need to add, at runtime, some specific handlers. 

<u>Description</u>:
Now through the ```MadServerPlugin.getConfiguration()```, we can customize the ```HandlerMapBuilder``` which is responsible for building an ```HandlerMap``` for each user session.

<u>Example</u>:
```java
// Builder
public class MyHandlerMapBuilder implements HandlerMapBuilder {
  ...
  public HandlerMap createHandlerMap(Object[[]] contextualInstances) {
    Map<String, Handler> myHandlers = createSpecificHandlers();
    return new MyHandlerMap(myHandlers);
  }
}

// HandlerMap
public class MyHandlerMap implements HandlerMap {
  ...
  public Handler getHandler(String handlerId) {
    return myHandlers.get(handlerId);
  }
}

// MAD server plugin configuration
public static class MyServerPlugin extends AbstractApplicationPlugin {
  public MyServerPlugin(MadServerPlugin madPlugin) {
    ....
    madPlugin.getConfiguration()
             .setHandlerMapBuilder(new MyHandlerMapBuilder(...));
  }
}

```

See [[codjo-mad - Handler construction principle]]
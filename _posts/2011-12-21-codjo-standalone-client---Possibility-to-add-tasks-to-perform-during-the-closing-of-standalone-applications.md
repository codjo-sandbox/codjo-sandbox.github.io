---
layout: post
title: agf-standalone-client - Possibility to add tasks to perform during the closing of standalone applications
tags: [framework-2-10,codjo-standalone-client]
---
<u>Context</u>

For standalone applications, it was not possible to perform tasks while closing the application.

<u>Description</u>

It is now possible to add tasks to perform during the closing of the application.

<u>Example</u>

```java
QuitAction quitAction = standaloneClient.getGlobalComponent(QuitAction.class);
quitAction.addQuitTask(new Runnable() {
      public void run() {
             Trigger trigger = new Trigger();
             trigger.cleanUser(Iris.getInstance().getUser().getId().getLogin());
      }
});
```


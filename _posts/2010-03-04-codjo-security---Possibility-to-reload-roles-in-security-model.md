---
layout: post
title: agf-security - Possibility to reload roles in security model
tags: [framework-1-137,codjo-security]
---
<u>Context</u>:
For ```damas``` application, we need to add roles associated with dynamically generated handlers.
These roles have to be visible in ```User Administration Gui```.

<u>Description</u>:
A new class ```SecurityServerPluginOperations``` has been created with ```reloadRoles``` method which updates current security model with roles read from the ```UserFactory```.

```java
securityServerPlugin.getOperations().reloadRoles(UserId.createId("myLogin", "myPassword"));
```

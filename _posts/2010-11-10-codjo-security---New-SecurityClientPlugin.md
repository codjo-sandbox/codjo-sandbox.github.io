---
layout: post
title: agf-security - New SecurityClientPlugin
tags: [framework-1-173,codjo-security,hot-topics]
---
<u>Context</u>:
We need to implement security for applications without database (scribe, sam, magic).
For this purpose, some code concerning security actually in ```MadConnectionPlugin``` will be moved to a new plugin: ```SecurityClientPlugin```.

<u>Description</u>:
For now, an empty ```SecurityClientPlugin``` has been created.
It must be added by applications using ```MadConnectionPlugin``` in order to be ready, in a future step, to be compatible with new deployed versions of ```MadConnectionPlugin``` and ```SecurityClientPlugin```.

```java|title=Before
guiClient.addPlugin(MadConnectionPlugin.class);
```

```java|title=After
guiClient.addPlugin(SecurityClientPlugin.class);
guiClient.addPlugin(MadConnectionPlugin.class);
```
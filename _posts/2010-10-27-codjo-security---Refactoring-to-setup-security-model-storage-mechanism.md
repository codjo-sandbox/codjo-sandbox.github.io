---
layout: post
title: agf-security - Refactoring to setup security model storage mechanism
tags: [framework-1-172,codjo-security]
---
<u>Context</u>:
We need to implement security for applications without database (scribe, sam, magic).
But current ```codjo-security``` implementation is overly coupled with database connection.

<u>Description</u>:
```codjo-security``` has been refactored to introduce the notion of security storage mechanism.
Such storage mechanism specify how security model is stored.
By now, available storages are ```jdbc storage``` (default storage mechanism) and ```file storage```.

```JdbcStorage``` is now responsible for creating the user connection pool.

```FileStorage``` can be configured via ```SecurityService.config``` 
```
SecurityService.config=storage.type=file|storage.file=<url_of your_file>
```

see: [[framework:codjo-security - Configuration de la persistance]]

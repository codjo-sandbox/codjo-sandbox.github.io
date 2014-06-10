---
layout: post
title: agf-sql - Ajout de la configuration du JdbcServerPlugin
tags: [framework-1-23,codjo-sql]
---
Ajout de la configuration du plugin ```JdbcServerPlugin```. Cet objet permet notamment de configurer les connections JDBC (driver, url, etc) par code sans passer par le fichier de configuration du server. 

**Remarque** : Les modifications par code sont surchargées par la configuration provenant du fichier ```server-config.properties```

<u>Exemple</u>
```java
JdbcServerPlugin plugin = ....
plugin.getConfiguration().setUrl("jdbc:sybase:Tds:ai-iris:34100");
plugin.getConfiguration().setCatalog("IRIS");
plugin.getConfiguration().setNumericTruncationWarning(true);
plugin.getConfiguration().setIdleConnectionTimeout(1_MIN):
...
``` 

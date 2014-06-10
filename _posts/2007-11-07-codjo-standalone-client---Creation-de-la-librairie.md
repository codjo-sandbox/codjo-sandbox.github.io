---
layout: post
title: agf-standalone-client - Creation de la librairie
tags: [codjo-standalone-client,framework-1-19]
---
Création de la librairie définissant le socle Plugin pour les applications client/serveur.

<u>Exemple d'utilisation</u> : 
```java
StandaloneClient client = new StandaloneClient(applicationData, new JukeBox());

client.addPlugin(JdbcServerPlugin.class);
client.addPlugin(SecurityServerPlugin.class);
client.addPlugin(SecurityGuiPlugin.class);
client.addPlugin(Alis2StandalonePlugin.class);

client.show();
```

---
layout: post
title: agf-confluence - Ajout des paramètres de connexion dans le ConfluencePlugin
tags: [framework-1-43,codjo-confluence]
---
Le plugin ```ConfluencePlugin``` n'a plus besoin de récuperer les paramètres de connexion à Confluence depuis la ```ContainerConfiguration```. Maintenant il suffit d'utiliser les "setter" suivants :

```
private String serverUrl;
private String user;
private String password;
private int timeout;
```

<u>Exemple</u>
```
ConfluencePlugin plugin = ...
plugin.getConfiguration().setUser("me");
```

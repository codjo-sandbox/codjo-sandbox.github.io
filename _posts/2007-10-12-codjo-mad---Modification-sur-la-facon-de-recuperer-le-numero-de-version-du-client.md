---
layout: post
title: agf-mad - Modification sur la façon de récupérer le numéro de version du client
tags: [framework-1-16,codjo-mad]
---
Jusqu'ici le plugin MadConnectionPlugin recherchait la méthode main dans la stack pour retrouver le nom de la classe applicative et donc son numéro de version. Dans le module iComp, la connexion ne se fait pas dans le main() donc l'approche décrite ci-dessus ne fonctionne pas.


A présent, on peut spécifier la classe main du module client pour que le plugin MadConnectionPlugin retrouve le numéro de version. Par exemple :

```
jadeClient.addPlugin(MadConnectionPlugin.class);
jadeClient.getPlugin(MadConnectionPlugin.class).setMainClass(ICompApplication.class);
```
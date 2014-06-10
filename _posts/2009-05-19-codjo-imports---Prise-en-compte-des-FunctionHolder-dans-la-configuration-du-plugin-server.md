---
layout: post
title: agf-imports - Prise en compte des FunctionHolder dans la configuration du plugin server
tags: [framework-1-96,codjo-imports]
---
<u>Contexte</u>
Dans un import il est possible d'appliquer des opérations sur les données à importer en s'appuyant sur un langage de script (issu d'```codjo-expression```) via les _FunctionHolder_.

<u>Problème</u>
Un import Rose a besoin de réaliser des opérations spécifiques sur les colonnes du fichier à importer que le langage de script ne propose pas par défaut.

<u>Solution</u>
Via la configuration du plugin _ImportServerPlugin_ il est désormais possible d'ajouter des _FunctionHolder_ spécifiques. 

```
   ImportServerPluginConfiguration importConfiguration = importServerPlugin.getConfiguration();
   importConfiguration.addFunctionHolder(new FilterFunctions());
```



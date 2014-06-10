---
layout: post
title: agf-confluence - Ajout d'un mécanisme de retry
tags: [codjo-confluence,framework-1-44]
---
Suite aux échec constants des appels utilisant l'API XML RPC, il a été nécessaire de mettre en place un mécanisme de retry.

La configuration de ce mécanisme s'opère par l'intermédiaire de la configuration du plugin ```ConfluencePlugin``` :
```
plugin.getConfiguration().setRetryCount(5);   // Nombre d'essais
plugin.getConfiguration().setRetryDelay(500); // Délai entre essais successifs en ms
```

Par défaut retryCount vaut 2 et retryDelay vaut 1000;
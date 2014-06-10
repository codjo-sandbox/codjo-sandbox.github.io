---
layout: post
title: agf-agent - Passage à Jade 3.5
tags: [codjo-agent,framework-1-21,hot-topics]
---
- Passage à Jade 3.5. Voici la [[synthèse du changelog Jade 3.5|DSI:Synthèse changelog Jade 3.5]].
- Ajout du NoConnectionIMTPManager permettant de bloquer la communication intra-platforme.
- L'utilisation des Story peut se faire avec ou sans le blocage de communication intra-plateforme. Le constructeur par défaut bloque la communication intra-plateforme.

Pour réactiver la communication intra-plateforme, la Story doit être instanciée avec le constructeur suivant :
```
Story story = new Story(Story.ConnectionType.DEFAULT_CONNECTION);
```

- Le passage à Jade 3.5 a aussi impacté quelques mocks suite à des changements d'interfaces côté Jade.

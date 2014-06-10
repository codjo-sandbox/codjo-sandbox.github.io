---
layout: post
title: agf-agent - Ajout d'une méthode factory sur AgentDescription
tags: [codjo-agent,framework-1-17]
---
Ajout d'une méthode permettant de construire la description d'un agent avant de s'enregistrer auprès du DF (Service de page jaune JADE).

<u>Exemple d'utilisation :</u>
```java
container.acceptNewAgent("my-job-agent", 
                         new MyJobAgent(DFService.createAgentDescription("dicid-retriever"))
                        ).start();
```

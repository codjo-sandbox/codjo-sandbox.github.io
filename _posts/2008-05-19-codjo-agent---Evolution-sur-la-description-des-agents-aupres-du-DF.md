---
layout: post
title: agf-agent - Evolution sur la description des agents auprès du DF
tags: [codjo-agent,framework-1-44]
---
Il est maintenant possible à un agent de décrire les protocoles, les ontologies ainsi que les languages qu'il est capable de gérer pour un service particulier.

<u>Exemple</u> : Déclaration d'un agent auprès du DF.
```java
import static com.agf.agent.DFService.service;
...
DFService.AgentDescription description = new DFService.AgentDescription();

description.add(service("product-provider", "mint-product-provider")
      .protocol("fipa-request")
      .ontology("product-ontology")
      .language("fipa-sl0", "fipa-xml-sl"));

DFService.register(me, agentDescription);
```


<u>Exemple</u> : Recherche d'un agent auprès du DF.
```java
import static com.agf.agent.DFService.service;
...
AgentDescription[[]] matches = 
   DFService.searchForService(me, 
                              service("product-provider").ontology("product-ontology"));
```

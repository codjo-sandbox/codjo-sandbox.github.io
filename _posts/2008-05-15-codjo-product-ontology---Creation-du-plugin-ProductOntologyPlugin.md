---
layout: post
title: agf-product-ontology - Création du plugin ProductOntologyPlugin
tags: [codjo-product-ontology,framework-1-44]
---
Introduction du ```ProductOntologyPlugin```. 

<u>Exemple</u> :
* Déclaration du plugin
```java
AgentServer server = ...
server.addPlugin(ProductOntologyPlugin.class);
```

* Pour encoder une demande de description d'un produit '007' à la date du '2003-01-01', il suffit de faire (utilisation de <u>fillMessage()</u>):
```java
ProductOntologyPlugin plugin = ...
ProductOntology productOntology = 
     plugin.getOperations().createProductOntology(agent);

GetProductAction request = new GetProductAction();
request.setCode("007");
request.setDate("2003-01-01");

productOntology.fillMessage(aclMessage, request);
```

* Pour decoder la requête (utilisation de <u>extractGetProductAction()</u>):
```java
ProductOntologyPlugin plugin = ...
ProductOntology productOntology  = 
     plugin.getOperations().createProductOntology(agent);

GetProductAction request = 
     productOntology.extractGetProductAction(aclMessage);
```

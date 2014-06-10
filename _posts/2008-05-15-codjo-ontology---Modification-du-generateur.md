---
layout: post
title: agf-ontology - Modification du générateur
tags: [codjo-ontology,framework-1-44]
---
Modification des beans produit par le générateur : 

* Utilisation des listes ```java.util``` à la place des listes ```jade.util.leap```
* Modification de l'héritage. Les beans implémentent des interfaces ```Concept``` ou ```AgentAction``` de ```codjo-ontology-common``` à la place des interfaces provenant de jade.
* Les listes sont ```generics``` : e.g. ```public List<StatusActor> getStatusActorList()...```


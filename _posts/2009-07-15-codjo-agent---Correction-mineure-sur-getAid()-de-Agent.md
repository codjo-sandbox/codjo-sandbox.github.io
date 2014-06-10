---
layout: post
title: agf-agent - Correction mineure sur getAid() de Agent
tags: [codjo-agent,framework-1-44]
---
La méthode ```getAid()``` de l'```Agent``` ne lance plus de ```NullPointerException``` lorsqu'elle est appelée avant que l'agent ne possède un identifiant. 

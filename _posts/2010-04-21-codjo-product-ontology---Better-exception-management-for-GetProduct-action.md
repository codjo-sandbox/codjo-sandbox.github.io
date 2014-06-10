---
layout: post
title: agf-product-ontology - Better exception management for GetProduct action
tags: [framework-1-143,codjo-product-ontology]
---
<u>Context</u>
When invoking the ```GetProduct``` action, some exceptions could raise due to model-checking problems. But due to a weak mapping in the jade WSIG layer (Web Service Integration Gateway), the cause of the exception was lost.

<u>Description</u>
The cause of model-checking exceptions is now encapsulated in the ```GetProductResponse``` bean. Thus, the client can really understand what happened in case of a model-checking error.

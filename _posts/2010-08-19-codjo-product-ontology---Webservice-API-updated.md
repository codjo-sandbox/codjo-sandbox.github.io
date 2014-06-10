---
layout: post
title: agf-product-ontology - Webservice API updated
tags: [framework-1-161,codjo-product-ontology,hot-topics]
---
<u>Context</u>:
Due to security issue, KSL has to provide a user and password to use the prodoc webservice.

<u>Description</u>:
* User and password have been added as parameters of the webservice (```GetProductAction``` now has the fields ```user``` and ```password```).
* The password is encrypted by the prodoc client, using a common key.
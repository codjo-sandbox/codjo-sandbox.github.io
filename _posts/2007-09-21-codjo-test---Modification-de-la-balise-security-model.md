---
layout: post
title: agf-test - Modification de la balise security-model
tags: [codjo-test,framework-1-13]
---
Ajout des attributs ```lastLogin``` et ```lastLogout```.

<u>Exemple :</u> 
```xml
<security-model user="user_tr" 
                roles="admin" 
                lastLogout="2003-01-01 01:00:00"/>
```
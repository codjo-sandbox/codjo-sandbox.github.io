---
layout: post
title: agf-security - Visibility of User related classes modified
tags: [framework-1-137,codjo-security]
---
<u>Context</u>:
In order to customise ```UserFactory``` for ```damas```, it was needed to use some package protected classes relied on ```User``` implementation.

<u>Description</u>:
Classes have been declared public and moved:
```com.agf.security.common.datagen.Pattern``` -> ```com.agf.security.common.api.Pattern```
```com.agf.security.common.datagen.Role``` -> ```com.agf.security.common.api.Role```
```com.agf.security.common.datagen.XmlUser``` -> ```com.agf.security.common.api.DefaultUser```

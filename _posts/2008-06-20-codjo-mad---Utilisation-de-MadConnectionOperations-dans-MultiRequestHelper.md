---
layout: post
title: agf-mad - Utilisation de MadConnectionOperations dans MultiRequestHelper
tags: [codjo-mad,framework-1-49]
---
Un nouveau constructeur permet d'utiliser ```MadConnectionOperations``` dans ```MultiRequestHelper``` au lieu de ```RequestSender``` :

```
public MultiRequestsHelper(RequestSender requestSender)
public MultiRequestsHelper(MadConnectionOperations operations)
```


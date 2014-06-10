---
layout: post
title: agf-confluence - ajout méthode moveAttachment dans plugin
tags: [codjo-confluence,framework-1-37]
---
Cette nouvelle méthode permet de déplacer / renommer un attachment d'une page.

```
confluenceOperations.moveAttachment(oldPageId, oldAttachmentName, newPageId, newAttachmentName);
```
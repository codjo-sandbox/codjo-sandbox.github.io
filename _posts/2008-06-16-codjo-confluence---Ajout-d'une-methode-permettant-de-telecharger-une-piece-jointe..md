---
layout: post
title: agf-confluence - Ajout d'une méthode permettant de télécharger une pièce jointe.
tags: [framework-1-45,codjo-confluence]
---
Il est possible de télécharger une pièce jointe d'une page confluence. Pour celà utiliser la méthode ```downloadAttachment``` de ```ConfluenceOperations``` :
```
File downloadAttachment(String pageId, String attachmentName, String targetDirectory)
    throws IOException, ConfluenceException;
```

**Exemple**
```
File downloadedFile = operations
    .downloadAttachment(myPage.getPageId(), myAttachmentName, "c:/dev/temp");
```

Seule la dernière version de la pièce jointe sera récupérée.
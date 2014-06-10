---
layout: post
title: agf-mad - Envoie de requêtes à partir du GuiContext
tags: [framework-1-19,codjo-mad,hot-topics]
---
Il est maintenant possible d'envoyer des requêtes au serveur en passant par le ```GuiContext```. La nouvelle méthode ```getSender()``` renvoie un objet de type ```Sender``` comportant un ensemble de méthode utilitaire pour l'envoie de requête au serveur (insert, select, update, delete, etc.).

<u>Exemple</u>
```java
Row row = guiCtxt.getSender().selectRow("selectCurrency", 
                                        new FieldsList("currencyCode", "EUR"));
String currencyLabel = row.getFieldValue("label");
```


<u>Exemple</u> il est aussi possible de récuperer le ```MadConnectionOperations```.
```java
guiCtxt.getSender().getConnectionOperations();
```

{note:title=Attention}
Cette nouvelle méthode d'envoie de message prend le pas sur les classes ```RequestSender``` et ```RequestHelper```. Ces 2 classes **ne doivent donc plus être utilisées**.
{note}



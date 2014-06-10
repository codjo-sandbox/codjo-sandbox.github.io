---
layout: post
title: agf-test - Amélioration de la classe MailFixture
tags: [codjo-test,framework-1-19]
---
Ajout d'une méthode permettant de vérifier la quantité de message reçu. 

<u>Exemple</u>:
```java
  mailFixture.assertReceivedMessageCount(1);
```

Ajout de la possibilité de vérifier les messages avec destinataire multiple

<u>Exemple</u>:
```java
  mailFixture.getReceivedMessage(0).assertThat()
           .from("gonnot@agf.fr")
           .to("USER1", "USER2")
           .subject("[[Plateforme Java]] Nouvelle version du framework - 1.18");
```


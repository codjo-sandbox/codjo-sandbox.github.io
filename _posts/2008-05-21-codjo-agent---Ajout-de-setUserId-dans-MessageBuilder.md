---
layout: post
title: agf-agent - Ajout de setUserId dans MessageBuilder
tags: [codjo-agent,framework-1-45]
---
Les méthodes ```setUserId(UserId userId)``` et ```setUserId(String login, String password)``` ont été rajoutées à ```MessageBuilder```.

<u>Exemple</u> : Création d'un message.

```java
import static com.agf.agent.test.MessageBuilder.message;
import static com.agf.agent.AclMessage.Performative.INFORM;

...

AclMessage aclMessage = message(INFORM).setUserId("login", "password").get();
```
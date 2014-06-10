---
layout: post
title: agf-agent - Amélioration de l'envoi de message par une Story
tags: [codjo-agent,framework-1-39]
---
L'envoi de message via ```Story``` a été amélioré. Un builder a été ajouté facilitant la construction du message.

#### Utilisation :

```java
import static com.agf.agent.AclMessage.Performative.INFORM;
import static com.agf.agent.test.MessageBuilder.message;

...

startReceiver("receiver1");
startReceiver("receiver2");

story.record()
   .startTester("sender")
   .send(message(INFORM)
      .to("receiver1", "receiver2")
      .usingProtocol("fipa-request")
      .withContent("do it"));

story.execute();
```
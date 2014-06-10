---
layout: post
title: agf-workflow - Suppression de abstract sur JobProtocolParticipant
tags: [codjo-workflow,framework-1-4]
---
Suppression de ```abstract``` du ```JobProtocolParticipant``` pour pouvoir traiter le cas ou l'on délègue l'execution du traitement a un autre ```Behaviour``` 

```java
participant = new JobProtocolParticipant();
participant.setExecuteJobBehaviour(myBehaviour);
```

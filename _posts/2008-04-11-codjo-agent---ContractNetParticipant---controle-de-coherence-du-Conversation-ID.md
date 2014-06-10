---
layout: post
title: agf-agent - ContractNetParticipant - contrôle de cohérence du Conversation ID
tags: [codjo-agent,framework-1-39]
---
Actuellement, si le Conversation ID n'est pas renseigné, le ```ContractNetParticipant``` cesse de répondre après ```accept-proposal``` ou ```reject-proposal```.
Afin d'indiquer au programmeur l'absence de ce Conversation ID, un warning console est affiché lors de la réception du ```cfp```.

#### Annexe :

![Alt attribute text Here](attachments/contract-net.jpg)
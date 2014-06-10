---
layout: post
title: agf-agent - Exception while executing two JobRequests of different type at the same time
tags: [framework-1-165,codjo-agent]
---
<u>Context</u>:
Working on ```ROSES```, there were errors when handler and notification JobRequest ran at the same time.

<u>Description</u>:
The ```conversationId``` used in the ```ContractNetInitiator``` wasn't unique enough, differents ```CFP``` could have the same ```conversationId```. In consequence, ```JobAgents``` could be asked to run the wrong ```JobRequest```.

It has been corrected.
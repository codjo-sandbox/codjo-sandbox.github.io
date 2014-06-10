---
layout: post
title: agf-agent - Improve Interaction with the AMS
tags: [framework-1-185,codjo-agent]
---
<u>Context</u>
For SAM we need to extract some data from message sent by the AMS (name of the Agent that did not receive an Alert).

<u>Description</u>
A new utility class ```AMSService``` has been added.

<u>Example</u>
```
AclMessage failureMessage = 
   agent.receive(and(matchPerformative(FAILURE),
                     matchSender(AMS)));
...
Aid failedReceiver = AMSService.getFailedReceiver(agent, failureMessage);
LOG.error(failedReceiver + " did not receive the alert.");
```

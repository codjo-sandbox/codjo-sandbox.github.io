---
layout: post
title: agf-agent - Add remaining steps in assertion error message of Story
tags: [codjo-agent,framework-1-152]
---
<u>Context</u>
If a ```Story``` recorder was set up with several steps but some of them were not executed as expected, the assertion error message would simply output
```
junit.framework.AssertionFailedError: agent 'bozo-agent' : story non termine
```
This message was not helpful at all to figure out which steps were left to be executed.

<u>Description</u>
The list of unexecuted steps is output in the new error message:
```
junit.framework.AssertionFailedError: steps restant pour 'bozo-agent': \
[[ReceiveMessageStep[(( Performative: INFORM ) AND ( Content: foobar )]]]
```

See [[Utilisation de codjo-agent]]
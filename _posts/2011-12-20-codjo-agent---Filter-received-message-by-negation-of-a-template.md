---
layout: post
title: agf-agent - Filter received message by negation of a template
tags: [framework-2-10,codjo-agent]
---
<u>Context</u>

Sometimes it's easier to specify a message template by the negation of a simple one.  Unfortunately, the framework does not offer such mechanism.

**NB:** A message template is the filter used by an agent behavior to receive messages (read its inbox).

<u>Description</u>

A new template method ```not(...)``` has been added to the ```MessageTemplate``` class.

<u>Example</u> : Build a message template that match all unexpected message.
```java
MessageTemplate expectedTemplateMessage = ...
MessageTemplate unexpectedTemplateMessage = MessageTemplate.not(expectedTemplateMessage);
...
addBehaviour(new MyDefaultBehaviour(expectedTemplateMessage));
addBehaviour(new UnexpectedMessageBehaviour(unexpectedTemplateMessage));
```


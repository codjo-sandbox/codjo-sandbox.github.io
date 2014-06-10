---
layout: post
title: agf-agent - Modification Story, addSubStep() devient add()
tags: [codjo-agent,framework-1-44]
---
La méthode ```addSubStep``` a été déclaré obsolète afin d'être remplacé par ```add```

<u>Exemple</u>
```java
story.record().startTester("ray-monde")
      .receiveMessage()
      .add(replyToGetProductActionWith(createProductResult()));
```
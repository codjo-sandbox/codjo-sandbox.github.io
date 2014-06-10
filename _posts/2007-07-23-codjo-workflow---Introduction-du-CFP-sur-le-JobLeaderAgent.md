---
layout: post
title: agf-workflow - Introduction du CFP sur le JobLeaderAgent
tags: [framework-1-6,codjo-workflow]
---
Introduction du mécanisme d'appel d'offre sur la branche Job. Le ```JobLeaderAgent``` recrute le ```JobAgent``` pour réaliser une tache en utilisant le protocol [[CFP|swdev:Protocoles de communication fipa]].

Par défaut le ```JobProtocolParticipant``` accepte toutes les requêtes et possède un skillLevel par défaut.

```java
protected SkillLevel getSkillLevel() 
    return SkillLevel.DEFAULT;
}

protected boolean acceptContract(JobContract contract) {
    return state == State.WAIT_FOR_REQUEST;
}
```

Pour changer ce comportement il suffit de surcharger les méthodes en question.
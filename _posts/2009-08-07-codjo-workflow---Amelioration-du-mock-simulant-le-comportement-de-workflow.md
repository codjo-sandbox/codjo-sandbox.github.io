---
layout: post
title: agf-workflow - Amélioration du mock simulant le comportement de workflow
tags: [framework-1-108,codjo-workflow]
---
La classe ```WorkflowSystem``` a été enrichie avec les méthodes suivantes :
* ```java
doNothingAfterJobReceived(String expectedJobRequestDescription);
```
Le système vérifie qu'il a reçu le ```JobRequest``` mais ne renvoie ni PRE ni POST.

* ```java
simulateJob(String expectedJobRequestDescription, SubStep... customBehavior);
```
Le système vérifie qu'il a reçu le ```JobRequest``` puis joue un comportement spécifique.

<u>Exemple</u> :
```java
story.record().mock(workFlowSystem())
              .doNothingAfterJobReceived(JOB_DESCRIPTION)
              .then()
              .simulateJob(JOB_DESCRIPTION, new SubStep() {
                  public void run(Agent agent, AclMessage message) throws Exception {
                      ...
                  }
              });
...
story.execute();
```
---
layout: post
title: agf-workflow - Normalisation de la configuration des timeouts
tags: [framework-1-62,codjo-workflow]
---
Introduction d'une classe permettant de configurer les timeouts (```WorkflowConfiguration```).
1. Cette classe sera accessible sur les plugins utilisant la couche workflow.
{<u>}Exemple{</u>} :
```java
// Configuration du timeout des imports de 5 secondes
importBatchPlugin.getConfiguration().getWorkflowConfiguration().setDefaultTimeout(5000);
```
1. Cette classe est utilisée par le ```ScheduleLauncher```. 
{<u>}Exemple{</u>} :
```java
// Configuration du timeout des imports de 5 secondes
ScheduleLauncher launcher = new ScheduleLauncher(myUserId);
launcher.setWorkflowConfiguration(myWorkflowConfiguration);
launcher.executeWorkflow(getContainer(), createImportRequest());
```

_Pour information_ il existe 2 timeouts :
** ```{**}myWorkflowConfiguration.setDefaultTimeout(...)*``` : désigne le timeout pour le workflow complet,
** ```{**}myWorkflowConfiguration.setDefaultReplyTimeout(...)*``` : désigne le timeout de la validité de prise en compte de la requête.
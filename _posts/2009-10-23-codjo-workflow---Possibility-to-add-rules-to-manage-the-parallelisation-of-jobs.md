---
layout: post
title: agf-workflow - Possibility to add rules to manage the parallelisation of jobs
tags: [framework-1-119,codjo-workflow]
---
In order to enable applications to customize the parallelisation of jobs, a new configuration system has been implemented.

There are two ways to configure the rules, sorted by decreasing priority:
1. by calling, in the server plugin initialisation:
```java
workflowServerPlugin.getConfiguration().addRulesFile(File yourCustomRulesFile);
or
workflowServerPlugin.getConfiguration().addRulesFile(URL yourCustomRulesFileUrl);
```
1. by adding the rules file ```workflow.drl``` into the ```META-INF``` resources directory in server module

Without any configuration a default rules file will be used that allows all jobs to run.

eg. [[codjo-workflow - Parallelisation]]
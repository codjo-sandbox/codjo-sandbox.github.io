---
layout: post
title: agf-workflow - Server configuration updated for suppression of JobFilter
tags: [framework-1-166,codjo-workflow]
---
<u>Context</u>
The use of ```JobFilter``` is too complex for the requirement.

<u>Descriptif</u>
The ```JobFilter``` is replaced by a ```List<String>``` which is used to filter ```Job```'s or ```JobRequest```'s request type.

The default configuration filters ```handler``` request types.

To configure another filter:
```
WorkflowServerPlugin workflowServerPlugin = ...

workflowServerPlugin.getConfiguration().registerJobFilter("my_request_type");
```
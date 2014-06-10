---
layout: post
title: agf-workflow - Modification du niveau de trace sur le Logger
tags: [framework-1-80,codjo-workflow]
---
Le niveau de trace sur le ```Logger``` est passé de info à debug sur la classe ```JobProtocolParticipant``` pour le type de trace suivant :
```
segmentation-job-agent INFO com.agf.workflow.common.protocol.JobProtocolParticipant  - Audit MID (C-1t38akv23fpmdt30j) -  / level=to-compute
```
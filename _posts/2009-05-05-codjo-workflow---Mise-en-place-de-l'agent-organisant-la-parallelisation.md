---
layout: post
title: agf-workflow - Mise en place de l'agent organisant la parallélisation
tags: [codjo-workflow,framework-1-96]
---
Branchement d'un agent de type ```OrganiserAgent``` entre les ```ScheduleLeaderAgent``` et le ```JobLeaderAgent``` dont le rôle est la planification des traitements de type workflow.

C'est cet agent qui aura la connaissance permettant la parallélisation (base de cas...).

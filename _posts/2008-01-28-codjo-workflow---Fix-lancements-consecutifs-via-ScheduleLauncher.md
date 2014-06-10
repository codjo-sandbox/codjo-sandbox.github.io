---
layout: post
title: agf-workflow - Fix lancements consécutifs via ScheduleLauncher
tags: [codjo-workflow,framework-1-28]
---
Le ScheduleLauncher réutilisait le même nickName lors de lancements successifs d'agents via executeWorkflow() ce qui pouvait causer une exception Jade lors du acceptNewAgent().

Un nouveau nickName est maintenant correctement recréé pour chaque nouvel appel.
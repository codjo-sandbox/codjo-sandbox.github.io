---
layout: post
title: agf-broadcast - Verifying the existence of property
tags: [framework-1-181,codjo-broadcast]
---
<u>Context:</u>
Orbis can't start because the context in ```BroadcastGuiPlugin``` doesn't contain the ```TranslationManager``` property.

<u>Description:</u>
The ```TranslationManager``` property is tested before being retrieved.
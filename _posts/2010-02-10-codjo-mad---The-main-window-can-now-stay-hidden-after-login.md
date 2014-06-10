---
layout: post
title: agf-mad - The main window can now stay hidden after login
tags: [framework-1-133,codjo-mad]
---
<u>Context</u>
As part of the gradual migration of ORBIS to the new JADE architecture, we don't want that the main window appears automatically after login.

<u>Description</u>
New method in ```MadGuiCore``` class :

```public void show(String[[]] arguments, ApplicationData applicationData, boolean showWindow)```

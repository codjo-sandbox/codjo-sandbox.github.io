---
layout: post
title: agf-control - Refactoring
tags: [framework-1-184,codjo-control]
---
<u>Context</u>
The ```RequestRecordCountField``` class defined in ```codjo-mad``` needs an explicit ```GuiContext``` parameter to be passed in its ```initialization``` method.

<u>Description</u>
The different calls to this method have been updated to match the new signature.

see: [[framework:/2011/01/26/codjo-mad - Refactoring to pass explicitly the GuiContext in RequestToolBar components]]
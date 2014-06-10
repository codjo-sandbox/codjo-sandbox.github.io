---
layout: post
title: agf-mad - Refactoring to pass explicitly the GuiContext in RequestToolBar components
tags: [framework-1-184,codjo-mad]
---
<u>Context</u>
For internationalization needs, the ```GuiContext``` had to be provided to ```RequestRecordCountField``` and ```RequestRecordNavigator``` components.

<u>Description</u>
The ```GuiContext``` is now passed explicitly in ```initialize``` methods of these components.
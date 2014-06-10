---
layout: post
title: agf-plugin - Plugin lifecycle refactoring
tags: [framework-1-193,codjo-plugin]
---
<u>Context</u>
* If no right are found during the login phase the application quit silently. This is not acceptable. 
* Moreover, the login GUI disappear during the login phase. This is not acceptable.

<u>Description</u>

* Heavy refactoring to introduce a plugin life-cycle object in the ```Core```.
* The lifecycle can be listened through a ```LifecycleListener```
* Now, the ```core.start()``` method launch the complete start phase of the core. For example: the ```plugin.initGui(GuiConfiguration)``` will also be called during the start phase.
* Now, the ```core.stop()``` method launch the complete stop phase of the core.
* The ```GuiPlugin``` has been templatized in order to unify the ```GuiPlugin``` from ```codjo-plugin``` and ```GuiPlugin``` from ```agf-mad```.

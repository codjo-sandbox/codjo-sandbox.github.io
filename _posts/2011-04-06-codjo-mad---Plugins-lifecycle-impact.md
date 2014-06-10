---
layout: post
title: agf-mad - Plugins lifecycle impact
tags: [framework-1-193,codjo-mad]
---
<u>Context</u>
* If no right are found during the login phase the application quit silently. This is not acceptable. 
* Moreover, the login GUI disappear during the login phase. This is not acceptable.

see: [[Plugins life-cycle|framework:/2011/04/01/codjo-plugin - Plugin lifecycle refactoring]]

<u>Description</u>

* ```codjo-mad``` use now the plugin life-cycle introduced in ```agf-plugin```. 
* The ```GuiPlugin``` of ```codjo-mad``` extends the ```GuiPlugin``` of ```agf-plugin```. 

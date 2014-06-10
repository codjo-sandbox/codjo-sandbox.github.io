---
layout: post
title: agf-referential - Refactoring of GuiCustomizer classes
tags: [framework-1-175,codjo-referential]
---
<u>Context :</u>
It was noticed that classes implementing ```GuiCustomizer``` interface, were messy. So, it was decided to refactor these classes.

<u>Description :</u>
This refactoring consists in 
* refactoring ```DefaultGuiCustomizer``` class
* making ```ReferentialItemPanel``` class to use a ```GuiCustomizer``` instead of private methods
* creating a ```GuiCustomizer``` handling audit panel
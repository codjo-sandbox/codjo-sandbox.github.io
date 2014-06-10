---
layout: post
title: agf-mad - Refactoring of FilterPanel to use GuiWrapper
tags: [framework-1-124,codjo-mad]
---
<u>Context</u>:
```FilterPanel``` class contained code which dealt with gui component values (including the mad NULL value).


<u>Description</u>:
```FilterPanel``` now uses ```GuiWrapper``` to get values from gui components.


See: [[framework:codjo-mad - Utilisation#filterpanel]]
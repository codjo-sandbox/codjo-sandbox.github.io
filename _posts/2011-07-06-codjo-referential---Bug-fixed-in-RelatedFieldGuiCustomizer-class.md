---
layout: post
title: agf-referential - Bug fixed in RelatedFieldGuiCustomizer class
tags: [framework-1-204,codjo-referential]
---
<u>Context :</u>
In some ```Smart``` project's detailed screens, there were some combo-boxes not showing their selected item.This failure was due to the fact that these combo-boxes were handled  by the wrong ```GuiCustomizer``` class.

<u>Description :</u>
The ```handle``` method in ```RelatedFieldGuiCustomizer``` is fixed.

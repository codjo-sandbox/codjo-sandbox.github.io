---
layout: post
title: agf-mad - GuiContext now contains components needed for internationalization
tags: [framework-1-179,codjo-mad]
---
<u>Context</u>
For internationalization needs, the GUI client has to access ```TranslationNotifier``` and ```TranslationManager``` references.

<u>Description</u>
```GuiContext``` is the main object used to store references throughout the whole GUI. It appears to be the best candidate to hold objects needed for internationalization.

All applications and libraries that depend on ```codjo-mad``` will retrieve internationalization references from ```GuiContext```.

Applications and libraries that do not depend on ```codjo-mad``` will retrieve internationalization references directly from the dedicated ```InternationalizationGuiPlugin``` from ```agf-i18n```.
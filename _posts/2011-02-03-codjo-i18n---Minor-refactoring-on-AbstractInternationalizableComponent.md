---
layout: post
title: agf-i18n - Minor refactoring on AbstractInternationalizableComponent
tags: [framework-1-186,codjo-i18n,api-change,codjo-mad,codjo-broadcast]
---
<u>Context</u>
Applications need to be internationalized. Therefore, all framework libraries that expose GUI components or contain messages dedicated to the user have to be internationalized too.

<u>Description</u>
```TranslationManager``` and ```TranslationNotifier``` parameters are no longer needed in the constructor.
---
layout: post
title: agf-i18n - Remove resources initialization
tags: [framework-1-194,codjo-i18n]
---
<u>Context</u>
In applications which add the ```InternationalizationGuiPlugin```, when a user tries to log with a wrong password, then it's not possible to log in with the correct password.

<u>Description</u>
Register of ```TranslationManager``` and ```TranslationNotifier``` resources was done in ```initContainer``` method.

To fix the bug we now register these resources in ```start``` method, and remove them in ```stop``` method.
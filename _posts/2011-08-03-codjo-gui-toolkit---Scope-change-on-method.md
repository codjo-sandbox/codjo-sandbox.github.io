---
layout: post
title: agf-gui-toolkit - Scope change on method
tags: [framework-1-207,codjo-gui-toolkit]
---
<u>Context</u>

In order to specialize&nbsp;an autocomplete JTextField behaviour, the ```JTextFieldAutoCompleter.showPopup()``` must be overriden.

<u>Description</u>

The method ```showPopup()``` has been scoped to ```protected``` instead of ```private```.
\\
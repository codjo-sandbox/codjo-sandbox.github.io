---
layout: post
title: agf-gui-toolkit - A parent component can be specified when using FileChooserManager and FilePathField classes
tags: [framework-1-164,codjo-gui-toolkit]
---
<u>Context</u>:
In some case (after an ```alt-tab``` for example) the file chooser window dialog was behind the main application window (blocking it) because it was not attached to a parent window.

<u>Description</u>:
Now a parent component can be specified using FileChooserManager and FilePathField classes.

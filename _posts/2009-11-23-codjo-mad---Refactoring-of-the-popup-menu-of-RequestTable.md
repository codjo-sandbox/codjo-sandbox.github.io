---
layout: post
title: agf-mad - Refactoring of the popup menu of RequestTable
tags: [framework-1-123,codjo-mad]
---
<u>Context</u>
When adding a new action in the ```RequestToolbar```, it is possible to set a boolean to add it to the popup menu too. Due to a JDK bug, the text displayed in the menu was not correctly set.

<u>Description</u>
Now, the text of the menu is explicitly set using the ```NAME``` property of the action.

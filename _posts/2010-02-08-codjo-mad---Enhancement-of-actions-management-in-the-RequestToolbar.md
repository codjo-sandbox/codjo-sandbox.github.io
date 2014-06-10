---
layout: post
title: agf-mad - Enhancement of actions management in the RequestToolbar
tags: [framework-1-133,codjo-mad]
---
<u>Context:</u>
See: [[framework:/2009/12/17/codjo-referential - Duplicate action (third edition)]]

<u>Description:</u>
Now, the method ```addMenuItemInPopUpMenu(JMenuItem menuItem, Position position)``` throws an exception if the position given in parameter is relative to another action missing in the popup menu.

<u>Exemple:</u>
```
//the code will throw an exception if the ACTION_ADD is missing in the popup menu
//  the boolean true indicates to add the action to the popup menu
toolBar.add(new MyGuiAction(context), "Mocked action", Position.left(ACTION_ADD), true);
```

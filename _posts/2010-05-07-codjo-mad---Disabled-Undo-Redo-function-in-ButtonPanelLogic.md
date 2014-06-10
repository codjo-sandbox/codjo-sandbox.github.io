---
layout: post
title: agf-mad - Disabled Undo-Redo function in ButtonPanelLogic
tags: [framework-1-146,codjo-mad]
---
<u>Context</u>:
```WaitingPanel``` can deadlock when used in conjunction with the undo/redo manager of ```ButtonPanelLogic``` (cf. the ```postEdit()``` method of ```UndoableEditSupport```).

<u>Description</u>:
```ButtonPanelLogic``` can now be constructed with a disabled undo/redo manager.

```
ButtonPanelLogic(ButtonPanelGui customizedGui, boolean enableUndoRedo)
```

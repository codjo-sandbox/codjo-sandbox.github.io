---
layout: post
title: agf-gui-toolkit - HyperLink component API enhanced
tags: [framework-1-130,codjo-gui-toolkit]
---
<u>Context</u>
The ```HyperLink``` component allowed to add actions to perform when clicking but methods allowing to remove actions were missing.

<u>Description</u>
API has been enhanced to allow to remove all actions or a specific action from the link.

```
public void removeActionListener(ActionListener actionListener);
public void removeAllActionListeners();
```
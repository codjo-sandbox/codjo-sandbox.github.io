---
layout: post
title: agf-mad - Prefix sur ButtonPanelGui
tags: [codjo-mad,framework-1-25]
---
Nous avons ajouté la possibilité de préfixer les boutons du ButtonPanelGui.

```
buttonPanelGui.setNamePrefix("MonPrefixe");
assertEquals("MonPrefixe.ButtonPanelGui.okButton", buttonPanelGui.getOkButton().getName());
```

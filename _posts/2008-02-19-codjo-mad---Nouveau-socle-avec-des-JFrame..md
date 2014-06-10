---
layout: post
title: agf-mad - Nouveau socle avec des JFrame.
tags: [codjo-mad,framework-1-32]
---
Mise en place d'un socle basé sur les ```JFrame```.

Ce socle possède les mêmes caractéristiques que le socle ```GuiClient``` (avec ```JInternalFrame```) : menu, toolbar, etc...

<u>Exemple</u> :
```java
GuiFrameClient guiClient = new GuiFrameClient(myMainPanel);
guiClient.addPlugin(SecurityGuiPlugin.class);
...
guiClient.show(arguments, applicationData);
```


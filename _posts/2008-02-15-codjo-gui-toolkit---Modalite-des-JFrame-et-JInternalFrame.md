---
layout: post
title: agf-gui-toolkit - Modalité des JFrame et JInternalFrame
tags: [codjo-gui-toolkit,framework-1-31,hot-topics]
---
#### JFrame
Le support de la modalité des ```JFrame``` a été mis en place.

Voici  un exemple d'utilisation :
```
JFrame parentFrame = ...
parentFrame.setVisible(true);

...

JFrame modalFrame = ...
modalFrame.setVisible(true);
Modal.applyModality(parentFrame, modalFrame);
```

#### JInternalFrame
Il est conseillé d'utiliser ```Modal.applyModality(...)``` au lieu de ```new Modal(...)```.



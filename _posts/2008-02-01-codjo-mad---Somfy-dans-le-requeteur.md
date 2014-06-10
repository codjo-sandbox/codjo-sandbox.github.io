---
layout: post
title: agf-mad - Somfy dans le requêteur
tags: [codjo-mad,framework-1-29]
---
Il est maintenant possible d'activer le Somfy dans le requêteur lors du click sur le bouton Valider.

How to:

```
...
FindAction findAction = (FindAction) getToolBar().getAction(FindAction.class);
findAction.setDisplayWaitingPanel(true);
...
```
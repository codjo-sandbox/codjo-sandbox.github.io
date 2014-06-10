---
layout: post
title: agf-segmentation - Passage en protected de CopyAction.isActivable()
tags: [codjo-segmentation,framework-1-86]
---
La méthode ```isActivable()``` de l'action ```CopyAction``` est passée en ```protected``` alors qu'elle était déclarée ```private``` auparavant. Cela engendrait un problème de compilation suite au refactoring des actions héritant de AbstractGuiAction.

Cf : [[/2009/03/05/codjo-mad - Refactoring des actions de la RequestToolBar]]
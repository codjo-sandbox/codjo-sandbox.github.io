---
layout: post
title: agf-gui-toolkit - Chainage des ReadOnlyManager
tags: [codjo-gui-toolkit,framework-1-25]
---
Il est possible de chaîner des **ReadOnlyManager** via la méthode **addSubReadOnlyManager**. De cette façon, lorsque l'état du ReadOnlyManager principal est modifié, les sous-ReadOnlyManager qui lui sont rattachés sont modifiés à leur tour.

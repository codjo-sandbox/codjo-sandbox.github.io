---
layout: post
title: agf-mad - Propagation des event des WindowListener vers les InternalFrameListener
tags: [codjo-mad,framework-1-33]
---
Dans l'environnement multi-fenêtré, les évenements générés sur une JFrame et capturés par les WindowListener sont désormais reportés sur les InternalFrameListener des JInternalFrame correspondantes.

Les évenements propagés sont :

- ouverture / fermeture,
- activation / désactivation,
- iconification / désiconification
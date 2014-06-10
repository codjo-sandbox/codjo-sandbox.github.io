---
layout: post
title: agf-release-test - Amélioration du message d'erreur des xmf
tags: [codjo-release-test,framework-1-101]
---
Lors d'un echec de test dans un xmf, le message d'erreur ne précisait que le nom du groupe à l'origine du problème.

Désormais, les paramètres du call-method, ainsi que leur valeurs associées, sont ajoutés à ce message.

Exemple :
```
"Step 1 du groupe 'Isr.xmf(@LaL_numberLine@=27 @simuLabel@=simu1 @ptfId@=PTF1 ):::PTF1 : Test du LaL' (SelectTabStep)"
```
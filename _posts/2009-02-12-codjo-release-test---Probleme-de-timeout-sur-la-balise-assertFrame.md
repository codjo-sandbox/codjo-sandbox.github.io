---
layout: post
title: agf-release-test - Problème de timeout sur la balise assertFrame
tags: [framework-1-83,codjo-release-test,hot-topics]
---
L'attribut ```timeout``` de la balise ```assertFrame``` était configuré à 0 dans le cas où l'on veut tester que la frame a bien disparu (attribut ```closed``` positionné à true). Ce positionnement perturbait les tests dans certains cas où la frame pouvait mettre un certain temps à se refermer (typiquement, dans le cas où la frame se refermait après un traitement long).

Ce bug a été corrigé.


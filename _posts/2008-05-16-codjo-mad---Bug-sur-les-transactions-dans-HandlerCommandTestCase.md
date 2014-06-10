---
layout: post
title: agf-mad - Bug sur les transactions dans HandlerCommandTestCase
tags: [codjo-mad,framework-1-44]
---
Dans le cas où l'on fait des ```insert``` dans un ```HandlerCommand``` en mode transactionnel, le test unitaire s'appuyant sur ```HandlerCommandTestCase``` génère une erreur lors de la vérification des ```output```.

```HandlerCommandTestCase``` a donc été modifié pour passer la connexion en auto-commit juste avant de lancer la comparaison avec les ```output```.
---
layout: post
title: agf-test-runner - Prise en compte de plusieurs paramétres pour la VM
tags: [codjo-test-runner]
---
Dans le fichier ```test-release.config``` le paramètre suivant ```vmParameter``` ne gérait qu'un seul paramètre.

Il est possible d'en définir plusieurs via ce même paramètre ou le nouveau paramètre : ```vmParameters```.


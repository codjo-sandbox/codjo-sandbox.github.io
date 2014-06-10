---
layout: post
title: agf-test - Correction du clic sur le header d'une JXTable
tags: [codjo-test,framework-1-50]
---
Un bug du ```clickTableHeader``` a été détecté lors de son utilisation avec une ```JXTable``` (cf. [[SwingX|swdev:SwingX]]) : le clic sur une colonne ne triait pas la table.
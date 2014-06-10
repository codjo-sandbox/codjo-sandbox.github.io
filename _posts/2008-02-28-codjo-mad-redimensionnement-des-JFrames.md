---
layout: post
title: agf-mad redimensionnement des JFrames
tags: [codjo-mad,framework-1-33]
---
Le système de multi-fenêtrage affectait la ```preferredSize``` de la ```JInternalFrame``` à la ```JFrame```.
Ce dimensionnement ne permettait pas d'afficher l'intégralité du contenu de la fenêtre.
Cette affectation de la taille a été supprimée : le ```pack()``` suffit \!
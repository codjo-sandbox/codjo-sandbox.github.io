---
layout: post
title: agf-tokio - Meilleure gestion de l'encodage des fichiers tokio
tags: [framework-1-113,codjo-tokio,resolution-of-brin,hot-topics]
---
{info}
Résolution de BRIN.
{info}

Précédemment, les fichiers ```tokio``` étaient chargés avec un encodage par défaut.
Maintenant, l'attribut ```encoding``` du fichier xml est lu afin de déterminer le jeu de caractères  utilisé pour la lecture du fichier.

Cette modification résout un bug rencontré dans Benchmark où le caractère euro n'était pas correctement géré par ```tokio```.

---
layout: post
title: maven-test-release-plugin - Gestion des traces lors d'un stop du serveur
tags: [framework-1-77,maven-test-release-plugin]
---
Le plugin n'affiche plus la stacktrace d'erreur dans le cas ou le stop du serveur local est en erreur (le cas le plus courant). Le comportement du mode local devient donc identique au mode distant. 

<u>Exemple</u> de trace : 
{noformat}
...
[[INFO] [test-release:stop-server]]
[[INFO]] shutdown localhost:35702
[[INFO]] exit-status: 0
...
{noformat}

---
layout: post
title: agf-agent - Cryptage du password dans UserId
tags: [framework-1-72,codjo-agent]
---
La méthode ```encode``` sur ```UserId``` renvoyait le mot de passe en clair. Il apparaît maintenant crypté, ce qui évite qu'il soit visible dans des logs.
---
layout: post
title: agf-agent - Correction encryptage et decryptage de l'UserId, problème de singleton.
tags: [framework-1-79,codjo-agent]
---
Dans la librairie **codjo-agent** on encrypte et décrypte les données relatives à l'utilisateur (login, password, loginTime).

Pour ce faire on utilise la librairie **codjo-crypto** et notamment l'objet ```StringEncrypter```.

Cet objet est utilisé sous la forme d'un singleton dans la librairie **codjo-agent**, dès lors il semblerait qu'il garde un certain état et l'encryptage et le decryptage ne se font pas bien.

**{<u>}Correction apportée{</u>}**: on instancie une nouvelle instance de&nbsp; ```StringEncrypter``` à chaque encryptage et décryptage au lieu d'utiliser un singleton.
\\
\\
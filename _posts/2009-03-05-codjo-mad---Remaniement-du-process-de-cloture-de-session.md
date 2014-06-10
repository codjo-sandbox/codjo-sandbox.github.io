---
layout: post
title: agf-mad - Remaniement du process de clôture de session
tags: [framework-1-86,codjo-mad]
---
Lors de l'arrêt d'un client (mort d'un ```PresidentAgent```), un ```KamikazeAgent``` est créé par le ```SecretaryGeneralAgent``` afin de clôturer la session et de libérer les ressources. En fin de traitement le ```KamikazeAgent``` se "suicide".

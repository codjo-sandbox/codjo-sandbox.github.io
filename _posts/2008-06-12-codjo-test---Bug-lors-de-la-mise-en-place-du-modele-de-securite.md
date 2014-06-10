---
layout: post
title: agf-test - Bug lors de la mise en place du modèle de sécurité
tags: [codjo-test,framework-1-48]
---
Un bug concernant la mise en place des modèles de sécurité a été soulevé dans ```Mint```.
Il survenait quand après une déconnection du client, le modèle de sécurité était mis à jour via ```<security-model>``` puis le client se reconnectait tout de suite après.

Ce bug était dû à la précision du  ```datetime Sybase``` qui est de l'ordre de 1/300s.
La date de mise à jour du modèle de sécurité stockée était vue comme identique par le système alors qu'il y avait eu deux insertions différentes mais espacées de seulement quelques ms.

Le bug a été corrigé en ajoutant un délai d'attente de 10ms avant et après l'insertion du modèle de sécurité.
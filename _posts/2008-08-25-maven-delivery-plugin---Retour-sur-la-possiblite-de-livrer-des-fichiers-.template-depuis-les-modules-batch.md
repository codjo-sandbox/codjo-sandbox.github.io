---
layout: post
title: maven-delivery-plugin - Retour sur la possiblité de livrer des fichiers .template depuis les modules batch
tags: [maven-delivery-plugin,framework-1-58]
---
Il n'est maintenant plus possible de livrer des fichiers .template dans les modules Batch des applis. Ceci est un retour sur la modification suivante : [[maven-delivery-plugin - Possibilité de livrer des fichiers templates pour les modules Batch|http://wp-confluence/confluence/pages/viewpage.action?pageId=4163773]].

Pour utiliser des variables Delreco dans les scripts .bat ou .sh, il est recommandé de procéder comme suit :
* Diviser le script en 2 fichiers, l'un contenant la configuration et les variables Delreco, et l'autre le script à proprement parler
* Copier la partie contenant les variables Delreco dans le répertoire /src/config
* Copier l'autre partie dans le répertoire /src/bin

Lors de la livraison, seuls les fichiers contenus dans le répertoire /config seront traités par Delreco.
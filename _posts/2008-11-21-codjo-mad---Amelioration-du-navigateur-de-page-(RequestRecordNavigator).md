---
layout: post
title: agf-mad - Amélioration du navigateur de page (RequestRecordNavigator)
tags: [framework-1-71,codjo-mad]
---
Le composant permettant de changer rapidement de page dans les RequestTable a été amélioré.
* Si la table n'a que 10 pages maximum, son fonctionnement ne change pas.
* Si la table a plus de 10 pages, les 10 premiers numéros seulement seront affichés (permettant une sélection rapide) avec en dessous une zone de saisie où on pourra entrer un numéro de page (touche 'entrée' du clavier pour valider).

Le focus sera automatiquement mis dans cette zone de saisie et son contenu déjà sélectionné pour permettre une saisie rapide.
* Si le numéro de page entré est supérieur au nombre de page maximum, le composant se comportera comme si le numéro de la dernière page avait été entré.

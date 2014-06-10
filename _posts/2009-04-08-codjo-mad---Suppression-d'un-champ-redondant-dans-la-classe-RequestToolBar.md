---
layout: post
title: agf-mad - Suppression d'un champ redondant dans la classe RequestToolBar
tags: [framework-1-89,codjo-mad]
---
La classe ```RequestToolBar``` comportait une instance de ```FindAction``` qui était pointée par 2 objets différents de la classe.

En effet, celle-ci comportait :

    * un champ findAction qui pointait vers cette instance de ```FindAction```
    * un objet Map<Class,Action> possédant cette même instance en tant que valeur associée à la clé FindAction.class

Ainsi, il a été décidé, avec l'accord de l'équipe transverse, de supprimer ce champs findAction, jugé redondant.

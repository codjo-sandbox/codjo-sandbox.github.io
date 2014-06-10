---
layout: post
title: agf-agent - Suppression d'un contrôle sur le mot de passe
tags: [framework-1-81,codjo-agent]
---
Dans la classe ```UserId```, le contrôle de la présence du caractère '/' était effectué sur le login et le mot de passe. 

Ces champs étaient concaténés en utilisant un '/' comme séparateur, le mot de passe y apparaissait crypté et au format hexadécimal. Il est donc inutile de contrôler la présence du '/' dans le mot de passe décrypté, et c'est pourquoi ce contrôle a été supprimé.

Le contrôle de la présence du '/' dans le mot de passe décrypté avait pour conséquence pour un utilisateur de ne pas pouvoir se connecter à une application si son mot de passe contient un caractère '/'.
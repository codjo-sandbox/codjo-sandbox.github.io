---
layout: post
title: agf-mad - Initialisation du login avec le DICID dans la fenetre de connexion
tags: [codjo-mad,framework-1-11]
---
Au lancement de l'application si un seul serveur est défini (en recette et en production) le champ "Compte" est&nbsp;initialisé avec&nbsp;le DICID de la session, sinon il est initialisé avec la valeur de la propriété "login.default.name".
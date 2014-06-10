---
layout: post
title: agf-test - WrongFieldException devient TokioLoaderException
tags: [codjo-test,framework-1-38]
---
Remplacement de **WrongFieldException** par **TokioLoaderException** pour pouvoir gérer différent types d'erreurs au chargement des ".tokio":

&nbsp;<u>Exception levée si</u>:
1. un champs d'une table du tokio est invalide,
1. on utilise la balise "include-story" en spécifiant un chemin incorrect du fichier tokio à inclure.
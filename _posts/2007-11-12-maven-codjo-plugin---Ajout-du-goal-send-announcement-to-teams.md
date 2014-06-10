---
layout: post
title: maven-agf-plugin - Ajout du goal send-announcement-to-teams
tags: [maven-codjo-plugin,framework-1-19]
---
Ajout du goal ```send-announcement-to-teams```. Ce goal permet d'envoyer le mail d'annonce à toutes les équipes lors de la stabilisation du framework. La liste des destinataires est récupérée de la page [[swdev:Destinataire equipe java]].

<u>Exemple</u> d'utilisation 
{noformat}
> super-pom
> mvn agf:send-announcement-to-teams
....
[[INFO]] ----------------------------------------------------------------------
[[INFO]] 
[[INFO]]    From    : GONNOT
[[INFO]]    To      : ...
[[INFO]    Subject : [Plateforme Java]] Nouvelle version du framework - 1.18
[[INFO]]    Body    : 
Bonjour,

Une nouvelle version du framework (POM entreprise) est disponible :

Version   : 1.18
Changelog : http://wp-confluence/confluence/display/framework/framework-1-18

Cordialement,
GONNOT
[[INFO]] Voulez-vous envoyer le mail ? (y/n)
{noformat}

---
layout: post
title: maven-agf-plugin - Ajout goal switch-lib-to-snapshot
tags: [framework-1-19,maven-codjo-plugin]
---
Nouveau goal permettant de basculer une librairie ou un plugin en SNAPSHOT dans le pom parent.

Attention, ce goal ne fait que modifier le pom parent, il ne fait ni commit, ni deploiement.

<u>Exemple</u> d'utilisation : ouverture de chantier sur la librairie common
{noformat}
> super-pom
> mvn agf:switch-to-snapshot -Dlib=common
....
BUILD SUCCESSFUL
{noformat}
<u>Exemple</u> d'utilisation : ouverture de chantier sur le plugin datagen
{noformat}
> super-pom
> mvn agf:switch-to-snapshot -Dplugin=datagen
....
BUILD SUCCESSFUL
{noformat}
<u>Exemple</u> d'utilisation : ouverture de chantier sur un plugin déjà en SNAPSHOT
{noformat}
> super-pom
> mvn agf:switch-to-snapshot -Dplugin=datagen
....
[[ERROR]] Deja en SNAPSHOT
[[INFO]] ------------------------------------------------------------------------
[[ERROR]] BUILD ERROR
[[INFO]] ------------------------------------------------------------------------
[[INFO]] Deja en SNAPSHOT
[[INFO]] ------------------------------------------------------------------------
{noformat}
<u>Exemple</u> d'utilisation : ouverture de chantier sur une librairie ou un plugin inconnu
{noformat}
> super-pom
> mvn agf:switch-to-snapshot -Dlib=maaad
....
[[ERROR]] Pas de libraire ni de plugin correspondant
[[INFO]] ------------------------------------------------------------------------
[[ERROR]] BUILD ERROR
[[INFO]] ------------------------------------------------------------------------
[[INFO]] Impossible de changer la version des librairies : Pas de libraire ni de plugin correspondant
{noformat}
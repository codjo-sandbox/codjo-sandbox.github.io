---
layout: post
title: agf-referential - Correction bug sur DefaultReferentialListGui
tags: [framework-1-56,codjo-referential]
---
Sur MINT, dans l'IHM des référentiels, nous avons observé un problème de fuite mémoire lorsque l'utilisateur faisait défiler rapidement la liste des référentiels à l'aide des flèches du clavier.

Ce problème provient du fait que la même instance de ```RequestTable``` est maintenue tout au long du cycle de vie de l'IHM et que la méthode ```setPreference``` de la ```RequestTable``` est appelée systématiquement à chaque changement de référentiel. Or, dans cette méthode, la réinitialisation du modèle n'est pas correctement réalisée, le nettoyage des anciens listeners n'étant pas bien effectué.

Afin de corriger ce problème de manière simple, le panel contenant la ```RequestTable``` et la ```RequestToolbar``` est maintenant recréé à chaque changement de référentiel.
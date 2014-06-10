---
layout: post
title: agf-mad - Corrections sur ButtonPanelLogic
tags: [framework-1-87,codjo-mad]
---
<u>Problème</u>
Le bouton _Archiver_ n'était désactivé que lorsque la _datasource_ principale était modifiée (Rappel de la règle de gestion de l'archivage dans l'exemple de MINT : on doit archiver le bench avant de procéder à toute modification). Or le benchmark est composé d'une liste d'indice. Si l'utilisateur ne modifiait que cette liste, le bouton _Archiver_ n'était pas désactivé.

<u>Solution</u>
Dès lorsqu'une sous datasource est ajoutée via la méthode _addSubDataSource(...)_, elle sera synchronisée avec le bouton Archiver.
Par ailleurs, le champ ```archiveManagerFactory``` était static. Il a été transformé en champ d'instance

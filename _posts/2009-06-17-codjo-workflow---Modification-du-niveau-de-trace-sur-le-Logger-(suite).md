---
layout: post
title: agf-workflow - Modification du niveau de trace sur le Logger (suite)
tags: [framework-1-100,codjo-workflow]
---
Le niveau de trace sur le ```Logger``` avait été passé de info à debug sur la classe ```JobProtocolParticipant``` pour les messages d'audit (cf. [[/2009/01/22/codjo-workflow - Modification du niveau de trace sur le Logger]]).

Par conséquent les erreurs n'étaient plus tracées.

Désormais si les messages d'audit contiennent des erreurs ils sont tracés au niveau info.

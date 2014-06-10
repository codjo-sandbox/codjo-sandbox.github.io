---
layout: post
title: agf-plugin - Optimisation de la gestion multi-thread du SessionManager
tags: [framework-1-86,codjo-plugin,hot-topics]
---
Le support du multi-threading de la classe ```SessionManager``` a été optimisé afin de réduire les possibilités de contention entre plusieurs threads (moins de zones synchrones).

<u>Conséquence</u> : Les implémentations des ```SessionListener``` doivent être thread-safe.

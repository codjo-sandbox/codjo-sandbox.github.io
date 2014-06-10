---
layout: post
title: agf-pom - Downgrade de commons-logging
tags: [framework-1-64,codjo-pom]
---
La version de commons-logging passe de 1.1.1 à 1.1.
Certaines librairies externes utilisant la version 1.1.1 ne prenaient pas en compte le paramétrage de log (habituellement log4J.xml).
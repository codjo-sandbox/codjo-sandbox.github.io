---
layout: post
title: maven-delivery-plugin - Modification du renomage .jnlp en .template
tags: [framework-1-20,maven-delivery-plugin]
---
Désormais le renommage s'éffectue correctement sans lever d'exception même si le fichier ```maConfig.jnlp.template``` existe déjà.\\
Le précédent fichier est effacé et remplacer. Si une telle opération n'est pas possible (protection du fichier, fichier déjà ouvert) alors une exception est levée.
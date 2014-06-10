---
layout: post
title: agf-database - Génération de scripts sql spécifiques aux différentes bases de données
tags: [framework-1-59,codjo-database]
---
La classe ```DatabaseScriptHelper``` a été enrichie pour permettre de générer différents scripts sql selon le type de base de données configuré.
Il est possible de générer des script de _drop_ (table, index et contrainte), de _create_ (index et contrainte) et des scripts de _log_ de création (table, index et contrainte).

Ce développement a été réalisé en vue de faire fonctionner ```datagen``` en multi-base.
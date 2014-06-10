---
layout: post
title: maven-database-plugin - Initialisation recursive
tags: [framework-1-19,maven-database-plugin,hot-topics]
---
Maintenant, le plugin database initialise recursivement la BD à partir des répertoires Objet SQL (table, procedure, etc.)

<u>Exemple</u> d'arborescence possible :
{noformat}
iris-sql/src/main/sql/
  |-table/
     |-alter/
     |-drop/
     |- AP_COMMON.tab
     |-processing/
        |-alter/
        |-drop/
        |- AP_TABLE.tab
{noformat}

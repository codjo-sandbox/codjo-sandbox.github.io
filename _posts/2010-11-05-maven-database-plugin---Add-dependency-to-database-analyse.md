---
layout: post
title: maven-database-plugin - Add dependency to database-analyse
tags: [framework-1-173,maven-database-plugin]
---
<u>Context</u>:
A modification of the ```codjo-database-analyse``` library is necessary and has to be taken into account by the database plugin.

<u>Description</u>:
During the installation of an application the database plugin was running with an old version of the database-analyse library even if it was in a SNAPSHOT version in the super-pom.
The problem is solved by adding the dependency.

see: [[framework:maven-database-plugin]]

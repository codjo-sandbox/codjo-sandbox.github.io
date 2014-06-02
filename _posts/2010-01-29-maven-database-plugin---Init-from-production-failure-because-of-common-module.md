---
layout: post
title: maven-database-plugin - Init from production failure because of common module
tags: [framework-1-132,maven-database-plugin]
---
<u>Context</u>:
In ```mint```, a ```mvn database:init-from-prod``` failed because ```mint-common``` module was ignored by the build whereas it was needed by ```mint-sql``` module.

<u>Description</u>:
Now, ```*-common``` modules are not ignored anymore.

---
layout: post
title: maven-database-plugin - Database configuration check during database comparison
tags: [framework-1-165,maven-database-plugin,hot-topics]
---
<u>Context</u>:
During database migration, it has been reported that compare-from-prod did not work due to different database parameters.

<u>Description</u>:
A new goal has been implemented to assert parameters are equals: assert-dataserver. This goal is plugged into compare-from-prod. It fails if database parameters are not the same.

Example of failure:
```
[[INFO]] database:assert-dataserver en execution...
[[ERROR]] goal 'com.agf.maven.mojo:maven-database-plugin:init-from-prod' en echec.
[[INFO]] ------------------------------------------------------------------------
[[ERROR]] BUILD ERROR
[[INFO]] ------------------------------------------------------------------------
[[INFO]] Le paramétrage de la base n'est pas correct ![Alt attribute text Here](attachments/)!

EXPECTED :
databaseServer = ad_daf1
databasePort = 34105
databaseBase = DAF_DEV1
databaseCatalog = DEVDB14
ACTUAL (C:\Dev\projects\red\red-sql\target\checkout\pom.xml) :
databaseServer = ai_red
databasePort = 34105
databaseBase = RED_INT
databaseCatalog = RED_INT
```

see: [[framework:maven-database-plugin]]
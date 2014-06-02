---
layout: post
title: maven-database-plugin - Database comparison fails when versionInProduction is not set in pom.xml
tags: [framework-1-128,maven-database-plugin]
---
<u>Context</u>:
In ```alis2```, when running ```mvn database:compare-from-prod -DversionInProduction=...```, comparison failed because ```versionInProduction``` argument was ignored and not present in ```pom.xml```.

<u>Description</u>:
```versionInProduction``` is now correctly used, consequently it allows to successfully run ```compare-from-prod``` even without ```versionInProduction``` tag in ```pom.xml```.
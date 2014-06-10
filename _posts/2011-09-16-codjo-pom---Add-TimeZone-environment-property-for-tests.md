---
layout: post
title: agf-pom - Add TimeZone environment property for tests
tags: [framework-1-211,codjo-pom,hot-topics]
---

<u>Context :</u>
Since jre15_06 is not windows seven compatible, timezone is set to GMT instead of Europe/Paris.
That may yeald issues in date comparison in tests.

<u>Description :</u>
As the timezone is badly resolved by jre15_06 on Windows seven, we have to specify it while executing tests.
A new environment property has been added in surefire plugin configuration.

N.B: One should add this environment property when executing tests in IntelliJ.
```
-Duser.timezone="Europe/Paris"  
 ```


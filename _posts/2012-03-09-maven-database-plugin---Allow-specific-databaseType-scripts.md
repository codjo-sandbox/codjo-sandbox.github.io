---
layout: post
title: maven-database-plugin - Allow specific databaseType scripts
tags: [framework-2-16,maven-database-plugin]
---
<u>Context</u>
We want to be able to switch easily from a databaseType to another one. 

<u>Description</u>
During the database initialisation phase the permissions scripts (grant and revoke) are dedicated to Sybase or Oracle as they are not generated.

Now :
* the scripts postfixed by another ```_databaseType``` are ignored,
* not postfixed scripts are executed in any case

<u>Example</u>

In a Sybase application the script ```grant_oracle.sql``` is ignored.

In an Oracle application the script ```grant_sybase.sql``` is ignored.






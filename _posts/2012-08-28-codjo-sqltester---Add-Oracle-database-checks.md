---
layout: post
title: agf-sqltester - Add Oracle database checks
tags: [codjo-sqltester]
---
<u>Context:</u>
On the Oracle PriceHub project, we couldn't verify the content of the SQL delivery file.

<u>Description:</u>
Now, some Oracle database checks have been introduced in order to verify this file.
The generated ```database.properties``` file in the project sql module is now used to get the database connection settings (i.e. ```my_project\my_project-sql\target\test-classes\database.properties```).

see: https://github.com/codjo/codjo-tools-sqltester/pull/1

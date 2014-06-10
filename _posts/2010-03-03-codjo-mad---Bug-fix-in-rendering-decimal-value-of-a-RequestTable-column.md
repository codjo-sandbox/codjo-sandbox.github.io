---
layout: post
title: agf-mad - Bug fix in rendering decimal value of a RequestTable column
tags: [framework-1-137,codjo-mad]
---
<u>Context</u>:
Columns of the ```RequestTable``` can be customized with preference (either by the XML file or else by java code) in which a custom renderer format can be set for number or date value.

In case of numbers, a renderer bug appears whenever the total number of digits is over than 17: The value is rounded and truncated.

For example the value **\-1540.10462413668716127000** with the format **\#,##0.####################** is rendered as follow: **\-1 540.104624136687**.

<u>Description</u>:
The above issue has been fixed.

<u>Example</u>:
Now the value **\-1540.10462413668716127000** with the format **\#,##0.####################** is rendered as follow: **\-1 540.10462413668716127**.
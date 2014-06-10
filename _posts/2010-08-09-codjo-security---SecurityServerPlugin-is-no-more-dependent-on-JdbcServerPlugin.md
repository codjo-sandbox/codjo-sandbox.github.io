---
layout: post
title: agf-security - SecurityServerPlugin is no more dependent on JdbcServerPlugin
tags: [framework-1-159,codjo-security]
---
<u>Context</u>:
Working with ```magic``` application, it was impossible to make it dependent on ```SecurityServerPlugin``` because ```magic``` has no database configured whereas ```SecurityServerPlugin``` depends on ```JdbcServerPlugin```.
Such dependency had been introduced by a previous work on ```codjo-security``` ([[framework:/2010/03/04/agf-security - Possibility to reload roles in security model]]).

<u>Description</u>:
```SecurityServerPlugin``` is no more directly dependent on ```JdbcServerPlugin```.
Instead, it uses the ```JdbcManager``` found in ```ApplicationCore``` to access database when needed.

see: [[framework:codjo-security]]

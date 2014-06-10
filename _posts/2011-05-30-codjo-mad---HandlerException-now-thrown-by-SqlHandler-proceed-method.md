---
layout: post
title: agf-mad - HandlerException now thrown by SqlHandler proceed method
tags: [framework-1-200,codjo-mad]
---
<u>Context</u> :
\\
In ```SqlHandler``` class, ```proceedSqlQuery()``` method called ```execute()``` method which does not propagate any Exception in some cases.
For example, this situation occurs when a stored procedure (without result set) generates a unique index violation.

<u>Description</u> :
\\
Exceptions are now correctly propagated by the call of ```executeUpdate()``` method instead of ```execute()``` method on the statement.
Consequently, ```proceed()``` method now throws a HandlerException in that cases.
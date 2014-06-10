---
layout: post
title: agf-control - Sql Connection was missing during execution of java type controls
tags: [framework-1-143,codjo-control]
---
<u>Context</u>:
Sql Connection was missing in the ```ControlContext``` of Java type Controls (classes that extend ```com.agf.control.common.AbstractControl```) during execution of controls <u>after import</u>.

--> ```getContext().getConnection```() was NULL in ```com.agf.control.common.AbstractControl```.

This problem does not exist when Java type controls were runned after a user input validation in request table (for example).

<u>Description</u>:
The problem has been corrected in the ```QuarantineControlManager``` class.
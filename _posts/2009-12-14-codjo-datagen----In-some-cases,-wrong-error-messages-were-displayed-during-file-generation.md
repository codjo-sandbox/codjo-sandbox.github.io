---
layout: post
title: agf-datagen -  In some cases, wrong error messages were displayed during file generation
tags: [framework-1-126,codjo-datagen]
---
<u>Context:</u>

During datagen generation, the use at the same time of special properties (like ```$\{table\```},&nbsp;```$\{className\```},&nbsp;```$\{SQLAttributes\```},&nbsp;```$\{SQLName:xxxx\```}) in datagen files and a 'datagen.properties' file, displayed wrong errors message like :
```
ERROR kernel.Util - Property ${SQLAttributes} has not been set
ERROR kernel.Util - Property ${table} has not been set
...
```
The special properties were wrongly considered as user properties which are normally replaced at this stage of the datagen generation. This is not the case for special properties. Hence, the error message was incorrect.

<u>Description:</u>

The problem has been corrected. The messages are not displayed anymore.


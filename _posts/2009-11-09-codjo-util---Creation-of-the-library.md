---
layout: post
title: agf-util - Creation of the library
tags: [framework-1-121,codjo-util,common-dispatching]
---
<u>Context</u>:
The library ```codjo-common``` should only be used by standalone applications but it was used for all types of applications and libraries. 
In order to dispatch the content of the library ```codjo-common``` and to clarify the dependencies, a new library ```agf-util``` has been created.

<u>Description</u>:
Two classes are available in this library:
* ```FileUtil``` which contains utilities methods to load, save and copy files.
* ```StringUtil``` which contains one method to remove all characters occurrences in a string.

see: [[codjo-util]]
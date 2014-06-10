---
layout: post
title: agf-standalone-common - Listener class added to audit operations in applications
tags: [framework-1-136,codjo-standalone-common]
---
<u>Context</u> :

We need to listen to ```Operation``` class ```save()``` method calls in order to add an audit service in several applications for the GACPA (IRIS, ALIS2,...).

<u>Description</u> :

In order to listen to the ```save()``` method, the following modifications were made :

* Creation of a new Interface : ```OperationSaveListener```
* Modification of existing Class : ```Operation```
**** new static field of type ```OperationSaveListener``` added, for a class scoped listener
**** new instance field of type ```OperationSaveListener``` added, for an instance scoped specific listener
**** ```save()``` method now calls appropriate ```OperationSaveListener``` if setted. If an instance scoped listener is setted, it will be notified instead of the static one.\\
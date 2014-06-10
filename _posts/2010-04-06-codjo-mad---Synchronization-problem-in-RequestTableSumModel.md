---
layout: post
title: agf-mad - Synchronization problem in RequestTableSumModel
tags: [codjo-mad,framework-1-141]
---
<u>Context</u>:

A ```NullPointerException``` was thrown when updating the ```RequestTable``` associated to the ```RequestTableSum```.


<u>Description</u>:

There was no synchronization in the ```RequestTableSumModel``` on the model of the ```RequestTable```. This caused ```NullPointerException``` on concurrent access to the model. Now updates of the ```RequestTableSumModel``` is carried out in a synchronization block.

See: [[codjo-mad - Utilisation]]
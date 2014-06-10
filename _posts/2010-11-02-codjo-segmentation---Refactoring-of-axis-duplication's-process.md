---
layout: post
title: agf-segmentation - Refactoring of axis duplication's process
tags: [framework-1-172,codjo-segmentation]
---
<u>Context</u>:
Since [[a previous modification in codjo-mad|framework:/2010/03/24/agf-mad - Closing the statement when proceeding sql query in SQLHandler class]], a new bug appeared during axis duplication. 

<u>Description</u>:
An ```HandlerCommand``` was created for this process instead of the classic ```SqlHandler```. 
In this implementation, the ```Statement``` isn't closed.
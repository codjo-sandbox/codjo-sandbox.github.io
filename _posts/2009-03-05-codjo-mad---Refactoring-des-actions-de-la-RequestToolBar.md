---
layout: post
title: agf-mad - Refactoring des actions de la RequestToolBar
tags: [codjo-mad,framework-1-86]
---
Un refactoring a été fait sur les actions ```AddAction```, ```EditAction```, ```DeleteAction```.
La méthode isActivable() de ```EditAction``` est protected alors que la même méthode sur  ```AddAction``` et ```DeleteAction``` est privée. La visibilité de cette méthode a été rendue protected sur chacune de ces actions.


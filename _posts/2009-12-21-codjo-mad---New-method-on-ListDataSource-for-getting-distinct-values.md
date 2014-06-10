---
layout: post
title: agf-mad - New method on ListDataSource for getting distinct values
tags: [framework-1-127,codjo-mad]
---
<u>Context</u> : 
In Ride, we need to get distinct not null values on a ```ListDataSource```.

<u>Description</u> : 
The method ```Set<String> getDistinctNotNullValues(String fieldName)``` has been added to the ```ListDataSource``` class.
It returns a ```Set``` of ```String``` without null value.

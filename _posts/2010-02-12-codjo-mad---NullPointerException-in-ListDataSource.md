---
layout: post
title: agf-mad - NullPointerException in ListDataSource
tags: [framework-1-134,codjo-mad]
---
<u>Context</u>:
The ```getDistinctNotNullValues(String fieldName)``` method of class ```ListDataSource``` throws a ```NullPointerException``` when the data source does not return any row.

<u>Description</u>:
In that case, this method now returns an empty set.

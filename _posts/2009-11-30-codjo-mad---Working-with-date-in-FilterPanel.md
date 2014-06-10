---
layout: post
title: agf-mad - Working with date in FilterPanel
tags: [framework-1-124,codjo-mad]
---
<u>Context</u>:
In some cases, it is useful to add a ```DateField``` in ```FilterPanel```.

<u>Description</u>:
Two methods have been added to ```FilterPanel```:
```java
void addDateFilter(String label, String componentName, String fieldName)

void addDateFilter(String label, DateField dateField, String fieldName)
```

![Alt attribute text Here](attachments/Snapshot 3.JPG)

See: [[framework:codjo-mad - Utilisation#filterpanel]]
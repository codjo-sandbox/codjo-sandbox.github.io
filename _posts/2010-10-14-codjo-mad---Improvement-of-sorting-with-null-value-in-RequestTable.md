---
layout: post
title: agf-mad - Improvement of sorting with null value in RequestTable
tags: [framework-1-171,codjo-mad]
---
<u>Context</u>:
"null" values were not correctly managed when sorting on string or date columns.


<u>Description</u>:
* In ```StringMadComparator```: the "null" string is now considered as less than any other string
* In ```DateMadComparator```: the unparsable values (like "null") were translate to a minimal date, which was 01/01/1970. Using a date that is before 01/01/1970 (like for example in test release) was problematic.
The unparsable values are now translated to a minimal date:
```
 private static final Date MIN_DATE;


    static {
        Calendar calendar = Calendar.getInstance();
        calendar.set(0, 0, 0, 0, 0, 0);
        MIN_DATE = calendar.getTime();
    }
```

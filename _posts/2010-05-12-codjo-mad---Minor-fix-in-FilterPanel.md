---
layout: post
title: agf-mad - Minor fix in FilterPanel
tags: [framework-1-147,codjo-mad]
---
<u>Context:</u>
A selector was built with every filter's value in the ```FilterPanel```, even if no value was selected (or typed). Therefore a character string ```"null"``` was present in the selector for each of these filters.

<u>Description:</u>
The selector has now only the non-null values of the panel's filters. The selector will return a primitive ```null``` when queried for a filter which has no selected value.

It is however still possible to modify the selector's content before use by overriding the protected method ```void preSearch(FieldsList)```.

See [[codjo-mad - Utilisation]]
---
layout: post
title: agf-mad - Enhancement of FilterPanel and SqlRequetor interactions
tags: [codjo-mad,framework-1-126]
---
<u>Context</u>:
When a ```SqlRequetor``` and a ```FilterPanel``` were used in the same gui, some interactions were conflicting: the Default ```LoadFactory``` used by the ```FilterPanel``` was lost.

<u>Description</u>:
* The bug has been fixed, it is now unnecessary to overwrite the handlerId each time the ```FilterPanel``` is used (case on roses for exemple).
* When the ```SqlRequetor``` is used, it cleans the filters of the ```FilterPanel```, this gives a better ergonomy to the user.


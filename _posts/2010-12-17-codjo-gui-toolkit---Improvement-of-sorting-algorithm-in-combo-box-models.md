---
layout: post
title: agf-gui-toolkit - Improvement of sorting algorithm in combo-box models
tags: [framework-1-179,codjo-gui-toolkit]
---
<u>Context :</u>
In the ```Smart``` project, performances of sorting combo-box items, were insufficient.

<u>Description :</u>
In ```ComboBoxModelSorter```, the "bubble sort" algorithm was used. By now, the method ```Collections.sort()``` is used to sort items.
In ```Smart``` project, sorting time decreased from 60 seconds to 10.
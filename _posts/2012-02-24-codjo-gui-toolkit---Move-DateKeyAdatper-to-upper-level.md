---
layout: post
title: agf-gui-toolkit - Move DateKeyAdatper to upper level
tags: [framework-2-16,codjo-gui-toolkit]
---
<u>Context</u>
For ```PriceHub```, we need to check if the user sets a correct formatted year (yyyy) when creating a calendar.

<u>Description</u>
The class ```DateKeyAdatper``` has been renamed to ```NumberKeyAdapter``` and extracted from ```DateField``` to check digits on a ```JTextField```.
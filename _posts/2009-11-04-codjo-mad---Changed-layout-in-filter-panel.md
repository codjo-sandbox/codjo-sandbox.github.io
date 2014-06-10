---
layout: post
title: agf-mad - Changed layout in filter panel
tags: [framework-1-120,codjo-mad]
---
The ```FilterPanel``` component used the ```FlowLayout``` by default. It made the rightmost filters go down when the window was resized to a size too small.

Now the ```BoxLayout``` is used.

![Alt attribute text Here](attachments/filterpanelboxlayout.PNG)
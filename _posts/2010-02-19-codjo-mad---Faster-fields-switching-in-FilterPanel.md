---
layout: post
title: agf-mad - Faster fields switching in FilterPanel
tags: [codjo-mad,framework-1-135]
---
<u>Context{</u>}There was a time lag when switching from a field to another in the ```FilterPanel``` component.

<u>Description{</u>}This time lag was due to dependant filters handling. It is now disabled when there are no dependant filters.

![Alt attribute text Here](attachments/FilterPanel.JPG)

See : [[codjo-mad - Utilisation]].
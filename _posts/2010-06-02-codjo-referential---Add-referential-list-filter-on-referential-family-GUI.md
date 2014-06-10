---
layout: post
title: agf-referential - Add referential list filter on referential family GUI
tags: [framework-1-149,codjo-referential]
---
<u>Context:</u>
For Mint application, a filter was needed to help users link referentials to families.

<u>Description:</u>
It has been done by adding:
- a textfield for typing the string to filter,
- a validation button which triggers the filter execution,
- a reset button which clears the textfield and the filter result.

After filter execution, the displayed referentials in the referential list are those which contain the string to filter.

Moreover, when changing the family selection, the filter is still applied.

<u>Example:</u>
![Alt attribute text Here](attachments/FilterRefFamily.JPG|align=center)
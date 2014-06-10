---
layout: post
title: agf-segmentation - Include another expression in a sleeve
tags: [framework-1-173,codjo-segmentation,hot-topics]
---
<u>Context</u>:
In segmentation we can't include sleeve expression correctly, it doesn't run if a column table reference is positioned before the include.

<u>Description</u>:
The bug is fixed, the 'include' runs correctly for all positions in the expression.

---
layout: post
title: agf-gui-toolkit - Improvement of the GroupableTableHeader's rendering
tags: [framework-1-190,codjo-gui-toolkit]
---
<u>Context:</u>
```{}GroupableTableHeader``` didn't take into account any header renderer set on the columns it is initialized with.

<u>Description:</u>
```{}GroupableTableHeader``` now paints the header using any preset column renderer.

see : [[GroupableTableHeader]]
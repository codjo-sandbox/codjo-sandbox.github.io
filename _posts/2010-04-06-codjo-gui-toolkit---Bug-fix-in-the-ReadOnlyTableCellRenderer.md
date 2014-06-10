---
layout: post
title: agf-gui-toolkit - Bug fix in the ReadOnlyTableCellRenderer
tags: [framework-1-141,codjo-gui-toolkit]
---
<u>Context</u>:
When the ```ReadOnlyManager``` is applied on the table, the ```PreferenceRenderer``` (set by default on the class ```String``` of the table) is ignored. So the column value is not well rendered when the table is readonly.

<u>Description</u>
The ```ReadOnlyTableCellRenderer``` has been fixed.
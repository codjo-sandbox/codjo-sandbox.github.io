---
layout: post
title: agf-gui-toolkit - The way to determine if a table column is easily sortable has been enhanced
tags: [framework-1-133,codjo-gui-toolkit]
---
<u>Context</u>
The class ```TableRendererSorter``` provides an easy way to sort columns of a ```JTable```. It manages automatically simple renderers such as ```DefaultTableCellRenderer``` or ```CheckBoxRenderer```. The problem is that when ```mad``` preferences are plugged into the table, such renderers are hidden behind a ```PreferenceRenderer``` that is used as an adapter. Trying to sort such columns then leads to an exception.

<u>Description</u>
The way to determine if a renderer is "simple" enough to provide an automatic sorting has been extracted into a protected method that can be overriden by classes that use specific renderers such as the ```mad``` library.

<u>Example</u>
```
protected boolean isSortableValue(TableCellRenderer cellRenderer, Object value, int row, int column);
```
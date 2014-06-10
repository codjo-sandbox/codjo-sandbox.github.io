---
layout: post
title: agf-mad - Sorting a column configured with a CheckBoxRenderer via preferences now works
tags: [framework-1-133,codjo-mad]
---
<u>Context</u>
When a ```CheckBoxRenderer``` is set upon a table column via the ```preferences.xml``` file, sorting this column does not work and leads to an exception.

<u>Description</u>
This bug was due to the fact that a ```PreferenceRenderer``` is used as an adapter for the underlying renderer defined in the ```preferences.xml``` file. 
By default the sorting mechanism implemented in ```gui-toolkit``` only considers ```DefaultTableCellRenderer``` and ```CheckBoxRenderer``` classes, not the ```PreferenceRenderer``` class, of course, which is mad-specific.
The sorting mechanism has been enhanced to take into account the "real" renderers hidden behind the ```PreferenceRenderer``` class by overriding the sorting mechanism defined in ```gui-toolkit```.
See [[framework:/2010/02/04/codjo-gui-toolkit - The way to determine if a table column is easily sortable has been enhanced]].
---
layout: post
title: agf-mad - Bug fix on the autocomplete combobox
tags: [framework-1-123,codjo-mad]
---
<u>Context</u>
When the user starts to type the beginning of the word stored in a large combobox, the combobox selects the last element.

The swingx API used to implement this kind of combo defines its own combobox editor which overrides the ```setSelectedItem``` method. And, the implementation of this method contains the method ```scrollToVisible``` which is responsible to select the last element of the combo.

<u>Description</u>
So, we override the editor to by-pass it. 


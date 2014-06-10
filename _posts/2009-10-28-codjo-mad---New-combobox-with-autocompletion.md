---
layout: post
title: agf-mad - New combobox with autocompletion
tags: [framework-1-118,codjo-mad,hot-topics]
---
User wants to select quickly a value in a combobox which contains a lot of items.

A new ```RequestComboBox``` called ```AutoCompleteRequestComboBox``` is available with autocompletion. So, when the user begins to edit, the combo selects the first item starting with the edited word.

<u>Example:</u>
```
// Instantiate combo like a RequestComboBox
RequestComboBox combo = new AutoCompleteRequestComboBox();
....
```
![Alt attribute text Here](attachments/autocompletecombobox.JPG)
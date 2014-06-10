---
layout: post
title: agf-gui-toolkit - Added method to force a text into a text field with autocompletion
tags: [framework-1-203,codjo-gui-toolkit]
---
<u>Context</u>
A ```JTextFieldAutoCompleter``` was set on a ```JTextField``` which value had to be changed programmatically. When calling ```JTextField.setText(String)``` on the graphical component, the autocompletion popup list appeared with the exact same value. This was considered as a problem since the user would not want to see this popup appear in that case.

<u>Description</u>
The new public method ```JTextFieldAutoCompleter.forceValue(String)``` was created to change the value in the text field component without triggering the popup. This method calls its parent class ```AutomaticCompletion.forceValue(String)``` which is protected.
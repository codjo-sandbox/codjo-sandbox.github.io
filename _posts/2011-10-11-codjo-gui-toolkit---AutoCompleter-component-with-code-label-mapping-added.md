---
layout: post
title: agf-gui-toolkit - AutoCompleter component with code-label mapping added
tags: [framework-2-2,codjo-gui-toolkit]
---
<u>Context</u>
ROSES needs an auto-complete textfield that displays labels to users but transmit code to the server.

<u>Description</u>
A ```JTextFieldCodeLabelAutoCompleter``` component has been added.

It works exactly the same as the ```JTextFieldAutoCompleter``` component except that instead of passing a ```Collection<String>``` as parameter, a ```Map<String, String>``` is passed to handle the mapping between codes and labels. Labels are displayed to users and methods such as ```forceCode(String code)``` and ```String getSelectedCode()``` have been added to interact with codes.
---
layout: post
title: agf-mad - RequestTextFieldAutoCompleter added
tags: [framework-2-2,codjo-mad]
---
<u>Context</u>
ROSES needs an auto-complete textfield that displays labels to users but transmit code to the server.

<u>Description</u>
A ```RequestTextFieldAutoCompleter``` component has been added. 

```
public RequestTextFieldAutoCompleter(JTextComponent textField,
                                     String handlerId,
                                     String keyColName,
                                     String labelColName)
```

The popup list displayed to users is loaded via the handler provided as parameter. Code and label values are taken from the field names passed as parameter. 
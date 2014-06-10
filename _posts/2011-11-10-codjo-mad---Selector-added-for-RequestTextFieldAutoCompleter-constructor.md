---
layout: post
title: agf-mad - Selector added for RequestTextFieldAutoCompleter constructor
tags: [framework-2-5-rc1,codjo-mad,framework-2-5]
---
<u>Context</u>

ROSES needed to use a handler with a selector to create a ```RequestTextFieldAutoCompleter``` component.
\\

<u>Description</u>

A new constructor had been added to the component.

```    public RequestTextFieldAutoCompleter(JTextComponent textField,
                                         String handlerId,
                                         String keyColName,
                                         String labelColName,
                                         FieldsList selector)

```
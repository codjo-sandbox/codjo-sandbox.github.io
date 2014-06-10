---
layout: post
title: agf-gui-toolkit - Getter added to NumberFieldEditor
tags: [framework-1-132,codjo-gui-toolkit]
---
<u>Context</u>

A subclass&nbsp;of&nbsp;```NumberFieldEditor``` needs to access the ```NumberField``` component from the overridden ```stopCellEditing()``` method.
\\

<u>Description</u>

The editor component of ```NumberFieldEditor``` has now a getter.

<u>Example</u>\\
```public abstract class WeightCellEditor extends NumberFieldEditor {
...

@Override
public boolean stopCellEditing() {
  if (getEditor().hasError()) {
    getEditor().setNumber(bean.getWeight());
  }
  return super.stopCellEditing();
  }
}
```
---
layout: post
title: agf-gui-toolkit - Protected scope for editor field of NumberFieldEditor
tags: [framework-1-131,codjo-gui-toolkit]
---
<u>Context</u>:

In Oscar, we need to access the ```NumberFieldEditor```'s editor field (of type ```NumberField```) from the ```stopCellEditing()``` method of a subclass.
\\

<u>Description</u>:

The ```NumberFieldEditor```'s editor field has now a&nbsp;protected scope.
\\

<u>Example</u>:
```public abstract class WeightCellEditor extends NumberFieldEditor {
  ...
  @Override   
  public boolean stopCellEditing() {
    if (editor.hasError()) {
      editor.setNumber(bean.getWeight());
    }
    return super.stopCellEditing();
  }
}
```
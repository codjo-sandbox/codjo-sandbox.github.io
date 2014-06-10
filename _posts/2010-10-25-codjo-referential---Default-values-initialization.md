---
layout: post
title: agf-referential - Default values initialization
tags: [codjo-referential,framework-1-172-rc2,framework-1-172,hot-topics]
---
<u>Context :</u>
For ```Damas``` project, it was asked to initialize default values for all detail screens.
For this development, some changes in ```GuiCustomizer``` interface were needed.

<u>Description :</u>
These changes consist of

* adding ```initDefaultFieldValue``` method in ```GuiCustomizer``` interface
* renaming ```AbstractGuiCustomizer``` class to ```GuiCustomizerAdapter```
* creating an new ```AbstractGuiCustomizer``` class with a ```declareField``` method's implementation
* implementing ```initDefaultFieldValue``` method in ```DefaultGuiCustomizer``` class

<u>Example:</u>
```
public void initDefaultFieldValue(Field field) {
        final String defaultValue = field.getDefaultValue();
        if ("boolean".equals(field.getType())) {
            ((JCheckBox)field.getComponent()).setSelected("1".equals(defaultValue));
        }

        if (field.isNumberField()) {
            ...
        }

        if ("string".equals(field.getType())) {
            ...
        }
    }
```

see: [[Default values initialization|framework:codjo-referential - Default values initialization]]
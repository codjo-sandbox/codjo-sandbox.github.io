---
layout: post
title: agf-mad - AutoCompleteRequestComboBox can be customized
tags: [framework-1-125,codjo-mad]
---
<u>Context</u>:
It was asked to Smart application to be able to insert dynamically new items in a combobox.

<u>Description</u>:
In the ```AutoCompleteRequestComboBox``` class, the new method ```getDataConverter``` was added. 
```
protected CustomBasicDataConverter getDataConverter()
```

It allows to override the ```CustomBasicDataConverter``` instance used by the class constructor. 
The class ```CustomBasicDataConverter``` contains the method 
```java
String[[]] getPossibleStringsForItem(Object item)
```
which returns values to display in the combo.

<u>Example</u>:
```java
public class MutableAutoCompleteRequestComboBox extends AutoCompleteRequestComboBox {
    @Override
    protected CustomBasicDataConverter getDataConverter() {
        return new MutableAutoCompleteDataConverter();
    }
}

class MutableAutoCompleteDataConverter extends CustomBasicDataConverter {
    @Override
    public String[[]] getPossibleStringsForItem(Object item) {
        String[[]] possibleItems = super.getPossibleStringsForItem(item);
        if (item == null || "".equals(item) || possibleItems.length == 0) {
            return new String[[]]{getValueTypedByUser()};
        }
        return possibleItems;
    }
}

```





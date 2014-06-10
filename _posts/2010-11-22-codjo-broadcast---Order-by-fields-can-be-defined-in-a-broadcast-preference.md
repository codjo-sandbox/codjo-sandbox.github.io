---
layout: post
title: agf-broadcast - Order by fields can be defined in a broadcast preference
tags: [codjo-sql,framework-1-175,codjo-broadcast,api-change]
---
<u>Context</u>
The ```Preferences``` API used to define the selector that will be used to get lines to export lacks of a "clean" way to define "order by" fields to be taken into account to sort lines in the different sections of the exported file.

The only way to get the lines sorted was to define the "order by" instruction in an expression linked to one of the tables used in the jointures, as follows:

```
public class MyPreferences extends Preferences {
...
    @Override
    protected void initJoinKeys() {
        addJoinKeys(INNER_JOIN, getComputedTableName(), getSelectionTableName(),
                    new String[[][]]```"SELECTION_ID", "SELECTION_ID", "="```);
        addJoinKeys(RIGHT_JOIN, getBroadcastTableName(), getSelectionTableName(),
                    new String[[][]]{
                          {"AGREEMENT_ENTITY_CODE", "AGREEMENT_ENTITY_CODE", "="},
                          {"PERIOD", "PERIOD", "="}
                    },
                    new JoinExpression("1=1 order by "
                                       <u> getSelectionTableName() </u> ".AGREEMENT_ENTITY_CODE, "
                                       <u> getSelectionTableName() </u> ".ITEM "));
    }
...
}
```

<u>Description</u>
A new method has been added to the ```Preferences``` API to define the "order by" to be used to sort lines when exporting the section.


<u>Example</u>

```
public class MyPreferences extends Preferences {
...
    @Override
    protected void initJoinKeys() {
        addJoinKeys(INNER_JOIN, getComputedTableName(), getSelectionTableName(),
                    new String[[][]]```"SELECTION_ID", "SELECTION_ID", "="```);
        addJoinKeys(RIGHT_JOIN, getBroadcastTableName(), getSelectionTableName(),
                    new String[[][]]{
                          {"AGREEMENT_ENTITY_CODE", "AGREEMENT_ENTITY_CODE", "="},
                          {"PERIOD", "PERIOD", "="}
                    });
    }


    @Override
    public OrderByField[[]] getOrderByFields() {
        return new OrderByField[[]]{new OrderByField(getSelectionTableName(), "AGREEMENT_ENTITY_CODE"),
                                  new OrderByField(getSelectionTableName(), "ITEM")};
    }
...
}
```

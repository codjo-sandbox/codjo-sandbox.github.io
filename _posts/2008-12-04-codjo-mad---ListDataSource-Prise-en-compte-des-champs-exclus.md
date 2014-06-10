---
layout: post
title: agf-mad - ListDataSource Prise en compte des champs exclus
tags: [framework-1-74,codjo-mad]
---
Lorsqu'un champ exclu est modifié, la ligne concernée ne doit pas être considérée comme nouvellement mise à jour.

```
   private Row setValueImpl(final int row, final String columnId, final String value) {
        (..)
        if (![Alt attribute text Here](attachments/updatedRows.contains(roww) && )addedRows.contains(roww) && !isExcludedOnUpdate(columnId)) {
            updatedRows.add(roww);
        }
        (..)
    }


    private boolean isExcludedOnUpdate(String columnId) {
        if (updateFactory != null && updateFactory instanceof UpdateFactory) {
            List<String> excludedFields = ((UpdateFactory)updateFactory).getExcludedFieldList();
            return excludedFields.contains(columnId);
        }
        return false;
    }
```
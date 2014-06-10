---
layout: post
title: agf-mad - Refactoring of Excel export actions
tags: [codjo-mad,framework-1-164]
---
<u>Context</u>
When using ```SpreadsheetExportAction``` or ```ExportAllPagesAction```, initialization of the list of tables to export, of their respective headers, of possible custom row iterators or renderer functor was done in separate methods.

For example, to use a custom header you would have to override ```setTableHeaderForBuilder```:

```java
class MyExportAction extends ExportAllPagesAction {
    MyExportAction(GuiContext ctxt, RequestTable table) {
        super(ctxt, table);
    }

    @Override
    protected void setTableHeaderForBuilder(RequestTable... tables) {
        List<Object[[][]> myHeaderList = createHeaderList(tables[0]]);
        builder.setHeaderData(tables[[0]], myHeaderList.toArray());
    }
}
```

If the row iterator had to be customized then ```createBuilder``` would have to be customized to override the ```getRowIterator``` method in ```ExportExcelBuilder``` class:

```java
class MyExportAction extends ExportAllPagesAction {
    MyExportAction(GuiContext ctxt, RequestTable table) {
        super(ctxt, table);
    }

    @Override
    public void createBuilder(RequestTable... tables) {
        builder = new ExportExcelBuilder() {
            @Override
            public Iterator<Row> getRowIterator(RequestTable table) {
                return createRowIterator(table);
            }
        };
        builder.setGuiContext(getGuiContext());
        builder.add(tables[[0]]);
        setTableHeaderForBuilder(tables);
    }
}
```

<u>Description</u>
Now the ```Action``` creates an ```ExportExcelBuilder``` which in turn configures appropriatly an ```ExportExcel``` object in charge of just one table with associated headers and iterator.

The following is the preferred way to override the default ```Action``` to customize the export:

```java
class MyExportAction extends ExportAllPagesAction {
    MyExportAction(GuiContext ctxt, RequestTable table) {
        super(ctxt, table);
    }

    @Override
    protected void createBuilder(RequestTable... requestTables) {
        Iterator<Row> myRowIterator = createRowIterator(requestTables[[0]]);
        List<Object[[][]> myHeaderList = createHeaderList(requestTables[0]]);
        builder.add(requestTables[[0]], myRowIterator, myHeaderList.toArray());
    }
}
```

If a header must be determined at 'action time' (when the action is triggered), one should override the ```doExport(ActionEvent)``` method:

```java
    [[...]]
    @Override
    protected void doExport(ActionEvent event) throws RequestException {
        builder.add(myRequestTable, myRowIterator, myHeaderList.toArray());
        builder.generate(exportAllPages());
    }
    [[...]]
```

See [[codjo-mad - Utilisation]]
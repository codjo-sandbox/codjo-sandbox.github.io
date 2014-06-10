---
layout: post
title: agf-mad - Refactoring of Excel export actions (2)
tags: [framework-1-166,codjo-mad]
---
<u>Context</u>
The [[last refactoring|/2010/09/09/codjo-mad - Refactoring of Excel export actions]] kept some methods that became obsolete and which name did not state clearly their purpose.

```title=com.agf.mad.gui.request.action.SpreadsheetExportAction
protected void createBuilder(RequestTable... tables)

protected void setTableHeaderForBuilder(RequestTable... tables)
```

```title=com.agf.mad.gui.util.ExportExcelBuilder
public ExportExcelBuilder add(RequestTable, boolean)

public ExportExcelBuilder setHeaderData(RequestTable, Object[[][]]...)
```

<u>Description</u>
The new refactoring is **not** compatible with old code. Some method signatures have changed, obsolete methods have disappeared, and the obsolete action ```ExportAction``` is deleted.

Typical cases of overriding taken from actual applications are shown below:

To customize the export action to change some headers on a table:
```title=com.agf.mint.gui.performance.calculPerfSimplified.ExportPerfResultAction
public class ExportPerfResultAction extends ExportAllPagesAction {
     public ExportPerfResultAction(GuiContext guiContext, RequestTable... tables) {
         super(guiContext, tables);
         setBuilder(new ExportExcelBuilder(guiContext)
               .add(tables[[0]],
                    new Object[[][]]```"Performances"```,
                    ExportExcelBuilder.createColumnHeader(tables[[0]]))
               .add(tables[[1]],
                    new Object[[][]]```"Historique Benchmark"```,
                    ExportExcelBuilder.createColumnHeader(tables[[1]]))
              }
}
```

To configure the export action when the action is triggered:
```title=com.agf.roses.gui.util.RosesQIdeeExportAction 
public class RosesQIdeeExportAction extends ExportAllPagesAction {
    public RosesQIdeeExportAction(GuiContext ctxt, RequestTable table) {
        super(ctxt, table);
        setBuilder(new ExportExcelBuilder(ctxt));
    }


    @Override
    protected void doExport(ActionEvent event) throws RequestException {
        String[[][]] headers = getHeaders();
        Iterator<Row> rowIterator = getSpecificRowIterator();
        builder.add(tables[[0]], rowIterator, headers);
        builder.generate(exportAllPages());
    }

    [[...]]
```

See [[codjo-mad - Utilisation]]
---
layout: post
title: agf-referential - New tree panel customizer
tags: [framework-1-123,codjo-referential,hot-topics]
---
<u>Context</u>
There are needs to customize the referential GUI.
For instance, it could be used to filter the tree on the left side.

![Alt attribute text Here](attachments/referentialTree.PNG|thumbnail)


<u>Description</u>
A ```TreeGuiCustomizer``` has been created to modify the ```ReferentialTreeGui```.


<u>Example</u>
```
public class OscarGuiPlugin extends AbstractGuiPlugin {

    public OscarGuiPlugin(ReferentialGuiPlugin refGuiPlugin) {
        refGuiPlugin.getConfiguration().setTreeGuiCustomizer(OscarReferentialTreeGuiCustomizer.class);
    }
}
```


```
public class OscarReferentialTreeGuiCustomizer implements TreeGuiCustomizer {

    public void init(ReferentialTreeGui referentialTreeGui) {
        JTree tree = referentialTreeGui.getReferentialTree();
        tree.setCellRenderer(new NiceRenderer());
    }
}
```


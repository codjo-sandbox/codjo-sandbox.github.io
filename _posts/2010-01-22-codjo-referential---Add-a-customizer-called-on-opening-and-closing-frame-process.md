---
layout: post
title: agf-referential - Add a customizer called on opening and closing frame process
tags: [framework-1-131,codjo-referential]
---
<u>Context</u>
For Damas project, we need to add a top panel during the referential frame's opening.

<u>Description</u>
Now it's possible to implement the interface ```ReferentialFrameCustomizer```.
```
public interface ReferentialFrameCustomizer {
    void handleFrameOpen(GuiContext context, ReferentialListGui listGui);


    void handleFrameClose(GuiContext context, ReferentialListGui listGui);
}
```

<u>Example</u>
```
public class DamasGuiPlugin extends AbstractGuiPlugin {

    public DamasGuiPlugin(ReferentialGuiPlugin referentialGuiPlugin, MadConnectionPlugin madConnectionPlugin)
          throws IOException, SAXException, ParserConfigurationException {
        configuration.setReferentialFrameCustomizer(DamasReferentialFrameCustomizer.class);
    }
}
```
```

  public class DamasReferentialFrameCustomizer implements ReferentialFrameCustomizer {

    public void handleFrameOpen(GuiContext context, ReferentialListGui listGui) {
        DamasModelBuilder builder = new DamasModelBuilder();
        builder.setGuiContext(context);
        FilterPanel filterPanel = new FilterPanel(builder);
        listGui.setTopPanel(filterPanel);
    }

    public void handleFrameClose(GuiContext context, ReferentialListGui listGui) {
        
    }

```


![Alt attribute text Here](attachments/filtre.JPG)

see: [[framework:codjo-referential - How to customize the referential GUI before the frame is opened]]

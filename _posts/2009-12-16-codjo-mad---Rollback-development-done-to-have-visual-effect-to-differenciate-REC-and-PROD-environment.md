---
layout: post
title: agf-mad - Rollback development done to have visual effect to differenciate REC and PROD environment
tags: [framework-1-126,codjo-mad]
---
<u>Context</u>:
The development made for the news [[framework:/2009/12/04/codjo-mad - Possibility to add an Observer during the construction of the main window's application]] is unnecessary.

The context of this news was : 
AAAm users need sometimes to launch their application in the REC/PROD environment at the same time. They 'd like to have visual effect to diffentiate them

<u>Description:</u>
We rollback the development.

<u>Example</u>
So, to add an Observer before the login:
```java
public class MyGuiPlugin extends AbstractGuiPlugin {
//......
    public void initGui(final GuiConfiguration guiConfiguration) throws Exception {
        configuration.getGuiContext().addObserver(new Observer() {
            public void update(Observable o, Object arg) {
                if (arg instanceof GuiEvent) {
                    GuiEvent guiEvent = (GuiEvent)arg;
                    if (guiEvent.getName().equals(GuiEvent.LOGIN.getName())) {
                       // change the UI
                       SwingUtilities.updateComponentTreeUI(
                             configuration.getGuiContext().getMainFrame());
                    }
                }
            }
        });    
    }
//......
}

```

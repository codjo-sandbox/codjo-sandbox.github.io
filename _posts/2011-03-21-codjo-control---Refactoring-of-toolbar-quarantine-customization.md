---
layout: post
title: agf-control - Refactoring of toolbar quarantine customization
tags: [framework-1-191,codjo-control]
---
<u>Context</u>
Since quarantine GUI settings are configured in ```quarantine.xml``` file, it seems better to put toolbar quarantine customization in this file instead of using the ControlGuiPluginConfiguration class.

See: [[framework:/2010/09/28/codjo-control - Customization of toolbar quarantine table]]


<u>Description</u>
A class, implementing the ```QuarantineToolbarCustomizer``` interface, have to be set in the quarantine GUI configuration file ```quarantine.xml``` using the ```toolbarCustomizer``` tag :

```
<quarantines>
    <gui name="My quarantine table">
        <window>
            ...
            <preference>QUserMaTable</preference>
            ...
            <toolbarCustomizer>com.agf.myApp.gui.MyToolbarCustomizer</toolbarCustomizer>
            ...
        </window>
    </gui>
</quarantines>
```

```
class MyToolbarCustomizer implements QuarantineToolbarCustomizer {
          public void customize(GuiContext ctxt, RequestToolBar requestToolBar) {    
              requestToolBar.removeAction(...);
              requestToolBar.addAction(...);
              ...
         }
      }); 
```
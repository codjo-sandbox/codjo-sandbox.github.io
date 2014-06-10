---
layout: post
title: agf-control - Customization of toolbar quarantine table
tags: [codjo-control,framework-1-169]
---
<u>Context</u>
We want to customize the toolbar of specific quarantine tables.

<u>Description</u>
It is now possible, for specific quarantine tables, to set a customizer method that is called after their default toolbar creation.

Code example :

```
ControlGuiPlugin controlGuiPlugin = ...

controlGuiPlugin.getConfiguration().setQuarantineToolbarCustomizer("QUserSharePriceWindow",
     new QuarantineToolBarCustomizer() {
          public void customize(RequestToolBar requestToolBar) {    
              requestToolBar.removeAction(...);
              requestToolBar.addAction(...);
              ...
         }
      }); 
```

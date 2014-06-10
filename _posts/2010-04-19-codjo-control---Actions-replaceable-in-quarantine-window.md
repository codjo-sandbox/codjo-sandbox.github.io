---
layout: post
title: agf-control - Actions replaceable in quarantine window
tags: [codjo-control,framework-1-143,hot-topics]
---
<u>Context</u>:

The only export action available in quarantine window was ```ExportAllPagesAction```. This action would only export visible columns of the ```RequestTable```.


<u>Description</u>:

It is now possible to replace the export action in the quarantine GUI configuration file ```quarantine.xml``` :

```xml
<gui name="Thingy" tooltip="Display thingies">
   <window>
      ...
      <preference>ThingyPreference</preference>
      <filter>thingyId</filter>
      ...
      <exportAction>com.agf.roses.gui.MyExportAction</exportAction>
      ...
   </window>
</gui>
```

It is also possible to replace the ```ValidationAction``` and the ```ForceAction``` in the same manner :

```xml
<gui name="Thingy" tooltip="Display thingies">
   <window>
      ...
      <validationAction>com.agf.roses.gui.MyValidationAction</validationAction>
      <forceAction>com.agf.roses.gui.MyForceAction</forceAction>
      ...
   </window>
</gui>
```

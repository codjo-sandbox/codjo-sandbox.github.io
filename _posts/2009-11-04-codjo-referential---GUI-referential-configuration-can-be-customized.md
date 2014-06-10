---
layout: post
title: agf-referential - GUI referential configuration can be customized
tags: [framework-1-120,codjo-referential]
---
<u>Context</u>:
For the ```DAMAS``` software we need to manage at runtime the referential window (add/remove tables).

<u>Description</u>:
Now the main referential configuration (aka ```ReferentialMapping```) can be customized through the ```ReferentialGuiPlugin.getConfiguration()```. All Standard configuration stuff (the XML file built by ```codjo-datagen```) has been regrouped in the ```XmlReferentialMapping``` class.

see: [[codjo-referential - How to customize the referential list at runtime]]

<u>Example</u>:
```java
// Referential Mapping
public class DamasReferentialMapping implements ReferentialMapping {
  ...
  public SortedMap<String, Referential> getReferentialsByPreferenceId() throws Exception {
      SortedMap<String, Referential> myReferentialMapping = ...;
      ...
      return myReferentialMapping;
  }
}

// Referential configuration
public static class MyServerPlugin extends AbstractApplicationPlugin {
  public MyServerPlugin(ReferentialGuiPlugin referentialPlugin) {
    ....
    referentialPlugin.getConfiguration()
             .setReferentialMapping(new DamasReferentialMapping(...));
  }
}
```

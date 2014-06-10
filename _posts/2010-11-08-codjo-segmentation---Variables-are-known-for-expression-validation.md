---
layout: post
title: agf-segmentation - Variables are known for expression validation
tags: [framework-1-173,codjo-segmentation,hot-topics]
---
<u>Context</u>
In Roses we use  expressions with some variables defined in the file ```segmentation-configs.xml```. When we validate the expression an error says that variables are unknown.

<u>Descriptif</u>
* Variables are now loaded in ```XmlFamilyPreference```.
* Type of the variable has been added.

```title=segmentation-configs.xml
<family-list ..>
  <family id="family_id" ..>
  ..
    <gui>
      <variables>
        <variable name="VAR_NAME" label="var_label" sqlType="varchar"/>
       </variables>
     </gui>
  </family>
</family-list>
```

see: [[framework:Documentation codjo-segmentation]]
---
layout: post
title: agf-datagen - Use of default value for referential database fields
tags: [framework-1-134,codjo-datagen]
---
<u>Context</u>:
Mint needs to use the default value of database fields to initialize the detail gui when creating a referential record.

<u>Description</u>:
While generating the ```ReferentialMapping.xml```, the default value of every field is now inserted, which was not the case before.

<u>Example</u>:
The default value ```1``` is set for the field ```isValuated```.
Before, the generated file was:
```
<field isGenerated="false"
       label="Valuated"
       name="isValuated"
       type="boolean"
       primary="false"/>
```

Now, the generated file is:
```
<field isGenerated="false"
       label="Valuated"
       name="isValuated"
       type="boolean"
       primary="false"
       default="1"/>
```
---
layout: post
title: agf-datagen - Remove application specific code in referential generation
tags: [codjo-datagen,framework-1-147,maven-datagen-plugin,hot-topics]
---
<u>Context</u>:
In the Mint application, a column of a referential can refer to another referential. Datagen resolves these dependencies with the ```foreign-key``` tag content and generates a handler id with the pattern ```selectAll$\{className\}WithCloseDate```. So, the generated handler id will be used by ```codjo-referential``` API to generate and fill a combobox for this column in the detail edition frame.

![Alt attribute text Here](attachments/referential.jpg)

<u>Description</u>:
This hack has been removed and been replaced by extending the ```referential``` tag. Now the column can be linked to a specific handler id within this tag.

<u>Example</u>:
```xml
<entity>
    <feature>
        ...
        <referential>
            <fill field="myColumn" handlerId="selectDataFromAnotherTable"/>
        </referential>
    </feature>

    <properties>
        ...
        <field name="myColumn" type="string">
            <description>A code</description>
            <sql precision="8" type="varchar"/>
        </field>
        ...
    </properties>
</entity
```

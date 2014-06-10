---
layout: post
title: agf-release-test - Add ClickRight step for EditCell step
tags: [framework-1-124,codjo-release-test,hot-topics]
---
<u>Context</u>:
On the CAPRI application, we need to test a popup menu action from a specific table cell. On the previous version of the ```codjo-release-test```, ```clickRight``` step was not allowed within an ```editCell``` step.

<u>Description</u>:
Now the ```clickRight``` step can be used within the ```editCell``` step.

see: [[codjo-release-test|http://wp-confluence/confluence/display/framework/agf-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-editCell]]

<u>Example</u>:
```
<editCell name="maTable" row="2" column="Colonne 2">
  <clickRight name="treeCellComponent" path="Bars:La Brocante:Bières:Leffe" select="Commander"/>
  <validate/>
</editCell>
```
---
layout: post
title: agf-release-test - New attributes on assertTree tag
tags: [framework-2-10,codjo-release-test,hot-topics]
---
<u>Context</u>

JTrees are rendered with JLabels including labels and icons.

<u>Description</u>

New attributes on ```assertTree``` tag ```foreground``` and ```icon``` allow to test icons and font colors.

```
<assertTree
   name="jobTree"
   path="null(Unknown):GROUPE 12(Unknown)"
   mode="model"
   exists="true"
   icon="question32.png"
   foreground="0,0,0"/>
```
see: [[codjo-release-test|http://wp-confluence/confluence/display/framework/agf-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-assertTree]]
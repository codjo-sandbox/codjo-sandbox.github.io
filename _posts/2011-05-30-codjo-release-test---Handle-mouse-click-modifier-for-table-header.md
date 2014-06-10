---
layout: post
title: agf-release-test - Handle mouse click modifier for table header
tags: [framework-1-200,codjo-release-test,hot-topics]
---
<u>Context :</u>
For ```Oscar``` project, it was needed to test table's header clicking actions with "Ctrl" or "Shift" keystroke.

<u>Description :</u>
A ```modifier``` attribute was added to ```ClickTableHeaderStep``` class allowing to specify the wanted keystroke.

<u>Example :</u>

```
<clickTableHeader name="ratingTable" column="0" modifier="ctrl"/>
```

see : [[documentation|http://wp-confluence/confluence/display/framework/codjo-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-clickTableHeader]]
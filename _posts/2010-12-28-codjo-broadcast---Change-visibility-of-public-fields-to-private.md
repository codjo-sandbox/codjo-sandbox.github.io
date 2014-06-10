---
layout: post
title: agf-broadcast - Change visibility of public fields to private
tags: [framework-1-180,codjo-broadcast]
---
<u>Context</u>

We used deprecated method from ```DetailWindowUtil``` class for fields declared as public :

```declarePublicFields(dataSource, frame)```
```manageFields(dataSource, frame)```

<u>Description</u>

We change visibility of declared fields as private. We replace usage of the deprecated methods by :

```declare(fieldName, fieldContainer)```
```manageEditModeFields(dataSource)```
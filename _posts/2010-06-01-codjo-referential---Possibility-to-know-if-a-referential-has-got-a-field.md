---
layout: post
title: agf-referential - Possibility to know if a referential has got a field
tags: [framework-1-149,codjo-referential]
---
<u>Context :</u>
For a Damas project's development, it was needed to know if a referential owns a field or not.

<u>Description :</u>
The ```hasField``` method has been added to ```Referential``` class. This method returns an boolean showing if the referential has a field with the given name.

<u>Example :</u>
```
boolean hasField = referential.hasField("fredField");
```
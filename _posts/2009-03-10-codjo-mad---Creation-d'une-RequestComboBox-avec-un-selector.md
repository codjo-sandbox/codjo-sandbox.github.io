---
layout: post
title: agf-mad - Création d'une RequestComboBox avec un selector
tags: [codjo-mad,framework-1-86]
---
La méthode ```createRequestCombobox``` a été surchargée dans la classe ```RequestComboBoxFactory```, afin de pouvoir utiliser un handler ayant besoin d'un selector

```
public static RequestComboBox createRequestCombobox(String handlerId,
                                                    String keyColName,
                                                    String labelColName,
                                                    boolean containsNull,
                                                    FieldsList selector)
```
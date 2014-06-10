---
layout: post
title: agf-referential - Creation GUI uses default value for database fields
tags: [framework-1-134,codjo-referential,hot-topics]
---
<u>Context</u>:
Mint needs to use the default value of database fields to initialize the detail gui when creating a referential record.
See: [[framework:/2010/02/15/codjo-datagen - Use of default value for referential database fields]]

<u>Description</u>:
The default value for each field is read from ```ReferentialMapping.xml```.
This value is used to initialize the corresponding field of the detail GUI, when creating a new record.

Theses types are correctly handled:
* ```boolean```
* numbers (```integer```, ```double```, ```big-decimal```, ```float```, ```long```)
* ```string```

{note:title=Be careful}
Others types will be ignored. Particularly, date types are not handled.
{note}

The foreign keys are correctly handled as well. This means that a combobox will automatically select the default value.

<u>Example</u>:
* if the default value of the boolean ```myBooleanField``` is set to ```1```, the corresponding checkbox will be ticked on the creation GUI,
** if the default value of the string ```myStringField``` (**without* foreign key) is set to ```'myDefaultString'```, the text of the corresponding text component will be set to ```myDefaultString``` on the creation GUI,
** if the default value of the string ```myStringField``` (**with* foreign key) is set to ```'myDefaultString'```, the ```myDefaultString``` item of the corresponding combobox will be selected on the creation GUI.

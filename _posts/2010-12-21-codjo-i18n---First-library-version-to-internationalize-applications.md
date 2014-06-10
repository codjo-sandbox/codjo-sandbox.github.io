---
layout: post
title: agf-i18n - First library version to internationalize applications
tags: [framework-1-179,codjo-i18n]
---
<u>Context</u>
```Mint``` application needs to be internationalized.

<u>Description</u>
The following classes have been created:

* ```TranslationManager```: this class is dedicated to store resource bundles and manage translations. Several properties files containing label keys and values in different languages can be registered.
```
public void addBundle(ResourceBundle resourceBundle, Language language);
public String translate(String key, Language language);
```

* ```TranslationNotifier```: this class is dedicated to change dynamically the labels of registered components when the language is modified by the user.
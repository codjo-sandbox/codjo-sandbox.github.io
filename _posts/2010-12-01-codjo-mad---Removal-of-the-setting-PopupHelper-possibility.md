---
layout: post
title: agf-mad - Removal of the setting PopupHelper possibility
tags: [framework-1-176,codjo-mad]
---
<u>Context :</u>
A previous modification on ```codjo-mad``` library (see : [[Possibility to specify a PopupHelper instance in a requestToolbar|framework:/2010/09/22/agf-mad - Possibility to specify a PopupHelper instance in a requestToolbar]]) wasn't accepted by the coach club. So, it was asked to rollback it.

<u>Description :</u>
The method ```setPopupHelper``` was deleted. 
In addition, for reasons of compatibility with ```Mint``` project which used this setting method (passing null as parameter), it was needed to add a method disabling the ```PopupHelper``` instance in ```RequestToolbar``` object.

<u>Example :</u>
```
 requestToolBar.disablePopupHelper();
```
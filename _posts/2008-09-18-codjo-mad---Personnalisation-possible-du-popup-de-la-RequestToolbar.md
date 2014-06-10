---
layout: post
title: agf-mad - Personnalisation possible du popup de la RequestToolbar
tags: [framework-1-58,codjo-mad]
---
La méthode ```getPopupMenu``` de la classe ```RequestToolBar``` a été rendue publique. Ceci permet de récupérer ce popupmenu et ainsi de le personnaliser.

<u>Exemple</u>:
```java
JPopupMenu popupMenu = requestToolbar.getPopupMenu();
popupMenu.add(new SpecificComputeAction(....));
```


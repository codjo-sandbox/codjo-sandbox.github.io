---
layout: post
title: agf-gui-toolkit - Enhancement of the error dialog
tags: [framework-1-123,codjo-gui-toolkit]
---
<u>Context</u>

* The error dialog (```ErrorDialog```) was unfortunately not resizable.
* Sometimes we were forced&nbsp;to cast ```Throwable```&nbsp;argument to&nbsp;```Exception.```

<u>Description</u>

* Now it is resizable.
* Some prototypes have been changed :

```
public static void show(Component aFrame, String message, Exception error)
/** is now **/
public static void show(Component aFrame, String message, Throwable error)
```

```
public static void show(Component aFrame, String message, String errorMessage, Exception error)
/** is now **/
public static void show(Component aFrame, String message, String errorMessage, Throwable error)
```
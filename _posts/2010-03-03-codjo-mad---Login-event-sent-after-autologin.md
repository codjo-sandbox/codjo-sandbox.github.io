---
layout: post
title: agf-mad - Login event sent after autologin
tags: [framework-1-137,codjo-mad]
---
<u>Context</u>:
(see: [[framework:/2010/02/17/codjo-mad - New event sent after application startup]])
The ```login event``` wasn't sent after autologin.

<u>Description</u>:
* The ```login event``` is now sent after autologin,
* The ```start event``` has been removed.

<u>Example</u>:
```java|title=In your application plugin
guiContext.addObserver(new Observer() {
  public void update(Observable o, Object arg) {
    if (arg == GuiEvent.LOGIN) {
       //Add your customisation here
    }
  }
});
```
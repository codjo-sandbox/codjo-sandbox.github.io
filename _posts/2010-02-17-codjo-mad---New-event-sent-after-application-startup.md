---
layout: post
title: agf-mad - New event sent after application startup
tags: [framework-1-134,codjo-mad]
---
<u>Context</u> :
For application damas, we need to customize the menu just after the main window opens. The login event was not enough as it doesn't work on 'autologin' mode.

<u>Description</u> :
A new event ```start``` is sent just after the main window shows.

<u>Example</u>:
```java|title=In your application plugin
guiContext.addObserver(new Observer() {
  public void update(Observable o, Object arg) {
    if (arg == GuiEvent.START) {
       //Add your customization here
    }
  }
});
```
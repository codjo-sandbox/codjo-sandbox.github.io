---
layout: post
title: agf-mad - Possibility to add an Observer during the construction of the main window's application
tags: [framework-1-125,codjo-mad]
---
<u>Context</u>
AAAm users need sometimes to launch their application in the REC/PROD environment at the same time. They 'd like to have visual effect to diffentiate them.

<u>Description</u>
We customize the look and feel for the main window after the connection.
So, we need to add an ```Observer``` to the ```GuiContext```, in the method ```show(...)```, to detect the moment when the user is connected. 

```java
public void show(String[[]] arguments, ApplicationData applicationData, Observer observer)
```

<u>Example</u>:
```java
// ...
guiClient.show(arguments, applicationData, new LoginObserver());
// ...

public class LoginObserver implements Observer {
    // ........ 

    public void update(Observable o, Object arg) {
        if (arg instanceof GuiEvent) {
            GuiEvent guiEvent = (GuiEvent)arg;
            if (guiEvent.getName().equals(GuiEvent.LOGIN.getName())) {
               // ........change the look and feel
            }
        }
    }
}
```


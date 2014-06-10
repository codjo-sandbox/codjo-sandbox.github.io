---
layout: post
title: agf-mad - Possibility to set the User in HandlerCommandTestCase
tags: [framework-1-138,codjo-mad]
---
<u>Context</u>:
In a ```damas``` software ```HandlerCommand``` test, it was needed to customise the ```User``` initiating the handler.

<u>Description</u>:
Method ```void setUserProfile(User)``` has been created in ```HandlerCommandTestCase```.
It allows to specify the ```User``` configured in ```HandlerContext```.

<u>Example</u>:
```java
public class SaveDamasModelCommandTest extends HandlerCommandTestCase {

    @Override
    protected void setUp() throws Exception {
        super.setUp();
        setUserProfile(myUserMock);
    }

...
}
```

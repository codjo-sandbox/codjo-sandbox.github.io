---
layout: post
title: agf-mad - Rendre forçable la casse du login
tags: [codjo-mad,framework-1-4]
---
Sur ```GuiClient.getConfiguration()``` création de la méthode ```setLoginCaseType``` permettant de forcer la casse du login.

Par exemple pour forcer le login en majuscule, il suffit dans la classe main applicative de faire 
```java

guiClient.getConfiguration()
         .setLoginCaseType(GuiClientConfiguration.LoginCaseType.UPPER_CASE);

```

Les choix possibles sont : 

```java
enum LoginCaseType {
    LOWER_CASE,
    UPPER_CASE,
    UNDEFINED
}
```

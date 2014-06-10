---
layout: post
title: agf-release-test - Cookie management implementation
tags: [framework-1-204,codjo-release-test,hot-topics]
---
<u>Context</u>:
Magic uses cookies to remember user's connection. This feature cannot be tested (release-test) as cookies are not managed by ```htmlunit```. 

<u>Description</u>:
Since ```htmlunit``` upgrade, it is possible to manage cookies by using a ```CookieManager```.

Now, by default, cookies are stored and shared between web-tests, wich is more realistic.
A new task has been added to be able to clear cookies.
 
see: [[clear-cookies|http://wp-confluence/confluence/display/framework/clear-cookies]]

<u>Exemple</u>:
```
   <clear-cookies/>

   <web-test url="http://patati/patata" session="ONE">
       <!-- the test creates some cookies -->
   <web-test/>

   <web-test url="http://patati/patata" session="TWO">
       <!-- session1 cookies are kept -->
   <web-test/>

   <clear-cookies/>

   <web-test url="http://patati/patata" session="THREE">
       <!-- there's no cookie available -->
   <web-test/>   

```
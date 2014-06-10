---
layout: post
title: agf-release-test - New attribute to enable SSL web tests
tags: [framework-2-11,codjo-release-test,hot-topics]
---
<u>Context</u>

It is actually not possible to make web tests in SSL context since it's not possible to specify any security information in ```web-test``` tags.

<u>Description</u>

To enable web testing in SSL environment, we add an attribute ```allowAllCertificates``` that tells the web client to accept any certificate from any host.

This value is true by default.   

<u>Example</u>
```xml

<web-test session="1"  url="https://localhost:8443/login"
  requestHeader="Accept-Language=fr,en;q=0.8,fr-fr;q=0.5,en-us;q=0.3"
  allowAllCertificates="true">
  
<assertPage title="Bienvenue sur Magic"/>
...
</web-test>
```

see: [[codjo-release-test|agf-release-test - Tags web#web-test]]
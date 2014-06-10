---
layout: post
title: agf-release-test - New attribute requestHeader available in web-test tag
tags: [framework-1-117,codjo-release-test,hot-topics]
---
The attribute ```requestHeader``` has been added to ```web-test``` tag.
It allows to set extra header properties to the request sent to the server.

<u>Example:</u>
```xml
<web-test url="http://localhost:8080/download/appli-gui.jnlp" 
          requestHeader="If-modified-since=Mon, 25 Dec 4090 11:58:00 GMT">
  ...
</web-test>
```

e.g. [[codjo-release-test - Tags web#web-test]]

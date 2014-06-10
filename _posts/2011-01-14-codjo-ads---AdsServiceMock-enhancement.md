---
layout: post
title: agf-ads - AdsServiceMock enhancement
tags: [framework-1-183,codjo-ads]
---
<u>Context</u>
To speed up application authentication during development phase for MAGIC, we need to enhance ```AdsServiceMock``` in order to replace any ADS development server.

<u>Description</u>
The method ```mockLoginBehaviour(...)``` has been added to ```AdsServiceMock``` to simulate error during login phase.

<u>Example</u>
```
AdsServiceMock adsService = new AdsServiceMock();
adsService.mockLoginBehaviour("system", new AdsSystemException("Haha, too bad fo you"));
...
adsService.login("system", "password"); // fails with an AdsSystemException
...
adsService.login("everythingElse", "password"); // authentication succeeds
```

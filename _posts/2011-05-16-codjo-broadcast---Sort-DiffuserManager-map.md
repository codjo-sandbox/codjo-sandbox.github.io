---
layout: post
title: agf-broadcast - Sort DiffuserManager map
tags: [framework-1-198,codjo-broadcast,jdk16-migration]
---
<u>Context</u>
During the JDK 6 migration impact study, we discovered that some unit tests failed because we were presuming of the diffusion map keys order.

see: [[framework:jdk16-migration]]

<u>Description</u>
The map of ```Diffuser``` in the ```DiffuserManager``` is now a ```TreeMap```.
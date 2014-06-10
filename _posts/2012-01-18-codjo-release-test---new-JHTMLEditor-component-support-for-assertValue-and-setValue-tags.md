---
layout: post
title: agf-release-test - new JHTMLEditor component support for assertValue and setValue tags
tags: [framework-2-12,codjo-release-test]
---
<u>Context</u>

As tinyMce HTML editor has been added to the framework, it can be used in java applications, but this component could not be tested in release tests.

<u>Description</u>

We modified the ```assertValue``` and ```setValue``` tags to enable release testing on HTMLEditor component.

N.B: Syntax has not changed.

see: 
 [[assertValue|framework:codjo-release-test - Tags IHM#assertValue]]
 [[setValue|framework:codjo-release-test - Tags IHM#setValue]]
 
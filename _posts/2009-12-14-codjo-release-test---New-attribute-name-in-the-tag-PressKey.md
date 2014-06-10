---
layout: post
title: agf-release-test - New attribute name in the tag PressKey
tags: [hot-topics,framework-1-126,codjo-release-test,resolution-of-brin]
---
<u>Context</u>:
{info:title=Resolution of BRIN}
AAAm test releases use the tag PressKey. Sometimes, Hudson build fails because the PressKey step is called, but the window doesn't have the focus.
{info}

<u>Description</u>:
Now, it's possible to add an attribute "name" to the PressKey tag. This attribute is the name of the component on which the user wants to simulate key inputs.

see: [[codjo-release-test | http://wp-confluence/confluence/display/framework/agf-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-pressKey]]
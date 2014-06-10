---
layout: post
title: agf-release-test - Add remote attribute in batch tag
tags: [framework-1-192,codjo-release-test]
---
<u>Context</u>
Delreco batch TR was disabled because its remote mode was not working.

<u>Description</u>
A ```remote``` attribute has been added to ensure that the batch will only be localy executed.
If this attribute is true, then the batch will follow the agf.test.remote configuration.

see: [[codjo-release-test|http://wp-confluence/confluence/display/framework/batch]]
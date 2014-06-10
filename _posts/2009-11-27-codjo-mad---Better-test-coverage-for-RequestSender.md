---
layout: post
title: agf-mad - Better test coverage for RequestSender
tags: [framework-1-124,codjo-mad]
---
<u>Context</u>

The XML serialization test for requests, ```RequestSenderTest```, didn't check field values containing the end character sequence of CDATA sections ("]]>"), even though it could cause a parsing error upon receipt.

<u>Description</u>

Such field values are now checked.
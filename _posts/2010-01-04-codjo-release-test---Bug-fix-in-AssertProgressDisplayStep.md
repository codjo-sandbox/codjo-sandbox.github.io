---
layout: post
title: agf-release-test - Bug fix in AssertProgressDisplayStep
tags: [framework-1-128,codjo-release-test]
---
<u>Context</u>:
```AssertProgressDisplayStep``` was still listening to the glass pane state even after it had been processed.

<u>Description</u>:
```AbstractAssertStep``` class has now a ```beforeStop()``` method, that can be overridden to allow some operations at the end of the ```proceed(TestContext context)``` method.

```AssertProgressDisplayStep``` overrides it to stop listening to the glass pane state.

see: [[codjo-release-test|http://wp-confluence/confluence/display/framework/agf-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-assertProgressDisplay]]
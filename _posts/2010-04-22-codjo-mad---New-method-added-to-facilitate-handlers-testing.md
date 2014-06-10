---
layout: post
title: agf-mad - New method added to facilitate handlers testing
tags: [framework-1-144,codjo-mad]
---
<u>Context</u>
```HandlerCommandTestCase``` provides a method allowing to test a handler execution in a nominal case. It does not enable to easily test exceptions thrown by the handler.

<u>Description</u>
A new method ```assertExecuteQueryWithFailure``` has been added.

```
protected void assertExecuteQueryWithFailure(String expectedMessage,
                                             String storyName,
                                             Map<String, String> arguments) throws SQLException;
```

This method allows to assert that ```expectedMessage``` is encapsulated in the exception thrown and checks the tokio output matching the given ```storyName``` parameter.

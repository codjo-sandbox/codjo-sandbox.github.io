---
layout: post
title: agf-workflow - Reactivation of handler job request log
tags: [framework-1-175,codjo-workflow]
---
<u>Context</u>:
Random failures occur while playing release test in hudson: a select handler fails in timeout.

<u>Description</u>:
```HandlerJobRequest``` log has been reactivated in order to check what happened in server side when such handler fails in timeout.

see: [[framework:/2010/09/06/codjo-workflow - Log4j logs handler-oriented messages at debug level]]
---
layout: post
title: maven-test-release-plugin - Make waitTimeBeforeCheckStatus field customisable
tags: [framework-2-58,maven-test-release-plugin]
---
<u>Context</u>
Delreco release tests sometimes fail because the server is not started when the first gui release-test tries to connect.
In fact, sometimes, the delreco server needs 6 seconds to start whereas the first test is executed only 3 seconds after the server start.

<u>Description</u>
see: https://github.com/codjo/maven-test-release-plugin/pull/1


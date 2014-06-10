---
layout: post
title: agf-release-test - Configuration property is no longer mandatory for Batch task
tags: [framework-1-140,codjo-release-test]
---
<u>Context:</u>
The ```Batch``` task is dedicated to test "generic" tasks in both local and remote ways. Nevertheless, it was not as "generic" as it should be because a "configuration" property was needed to execute the task.

<u>Description:</u>
The "configuration" property is no longer necessary to execute the task.

see: [[framework:batch]]
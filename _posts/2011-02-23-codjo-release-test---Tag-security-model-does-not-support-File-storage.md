---
layout: post
title: agf-release-test - Tag security-model does not support File storage
tags: [framework-1-188,codjo-release-test]
---
<u>Context</u>
Sam's administration client needs authorisation mechanism. As Sam doesn't relies on any database, the security-model tag can't be used. In facts, only database storage strategy is supported.

<u>Description</u>
We add the support for FileStorage strategy in security-model tag.

see: [[framework:security-model]]
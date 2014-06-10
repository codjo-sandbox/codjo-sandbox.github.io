---
layout: post
title: agf-release-test - Bug in release tests working with multi session
tags: [framework-1-157,codjo-release-test]
---
<u>Context</u>:
There was a bug with release tests using multi session (```gui-test session="XXX"```) when two gui-test sessions were running at the same time.

<u>Description</u>:
Before, in a gui step, the right component was not found. Now, it is fixed.

see: [[framework:codjo-release-test - Tags IHM#gui-test]]

<u>Reminder</u>:
```xml|title=How to use multi session in release tests
<gui-test session="session1">
...
</gui-test>

<gui-test session="session2">
...
</gui-test>

<gui-test session="session1">
...
</gui-test>
```

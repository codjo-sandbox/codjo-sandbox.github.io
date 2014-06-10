---
layout: post
title: agf-release-test - New tag file-exist-assert
tags: [framework-1-131,codjo-release-test,hot-topics]
---
<u>Context</u>:

In Ride project, we need to assert that some files are generated and others are not.

<u>Description</u>:

A new tag ```file-exist-assert``` has been added to fulfill this need.

<u>Example</u>:
```<file-exist-assert expected="true" filename="ExistingFile.txt"/>
<file-exist-assert expected="false" filename="MissingFile.txt"/>
```see [[assert-file-exists]]
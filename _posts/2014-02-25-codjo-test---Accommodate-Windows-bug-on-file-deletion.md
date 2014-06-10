---
layout: post
title: agf-test - Accommodate Windows bug on file deletion
tags: [framework-2-58,codjo-test]
---
<u>Context</u>
The ```CommandFileTest``` often fails on jenkins, because the ```DirectoryFixture``` can't delete some directories.

<u>Description</u>
see: https://github.com/codjo/codjo-test/pull/13
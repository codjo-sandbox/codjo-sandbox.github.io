---
layout: post
title: agf-test - Improve tearDown of the DirectoryFixture
tags: [framework-2-16,codjo-test]
---
<u>Context</u>
In some specific case, the deletion of the temporary directory created by the ```DirectoryFixture``` failed. 

<u>Description</u>
The ```tearDown()``` of the ```DirectoryFixture``` has been improved. Now, the teardown method will retry ten times with a short pause to delete the temporary folder before throwing an error.

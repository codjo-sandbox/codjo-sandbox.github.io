---
layout: post
title: maven-test-release-plugin - Bad deletion strategy on windows deployments
tags: [framework-1-192,maven-test-release-plugin]
---
<u>Context</u>
The Batch module of Delreco was not correctly deployed on its Windows server.

<u>Description</u>
After that the batch has been successfully deployed, its directory was deleted by the server  deployment.
Now, each deployment deletes only the remote directory concerned by the delivery zip.

---
layout: post
title: maven-test-release-plugin - Unix test resource deployment without shell file
tags: [framework-1-192,maven-test-release-plugin]
---
<u>Context</u>
The deployment of test resources forced us to add a dummy sh file.

<u>Description</u>
During the deployment a chmod was always executed and raised on error if no shell file was present.

Now the chmod is done only if shell files are present in the zip file to deploy.
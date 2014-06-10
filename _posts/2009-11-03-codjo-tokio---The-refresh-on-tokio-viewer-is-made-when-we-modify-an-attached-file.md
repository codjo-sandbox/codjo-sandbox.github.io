---
layout: post
title: agf-tokio - The refresh on tokio-viewer is made when we modify an attached file
tags: [framework-1-120,codjo-tokio]
---
When we modified either an entity or a tokio file specified in a ```include-story``` tag in the visualized tokio file, the data on ```tokio-viewer``` were not reloaded with these modifications.

Now when the ```tokio-viewer``` gains focus, tokio file is reloaded if the modification dates of attached files have changed.

see:[[codjo-tokio - Outil tokio-viewer|agf-tokio - IHM tokio-viewer]]

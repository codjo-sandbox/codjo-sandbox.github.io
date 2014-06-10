---
layout: post
title: agf-tokio - Rollback of modifications about timestamp comparison
tags: [framework-1-121,codjo-tokio]
---
<u>Context</u>:
This task is part of the _"```jconnect``` wrapper migration"_.

<u>Description</u>:
Recent modifications (see: [[/2009/10/26/codjo-tokio - Change in timestamp comparison]]) have been rollbacked.
The purpose of this modification is to have similar behaviour wih timestamp running either tokio test or application code.

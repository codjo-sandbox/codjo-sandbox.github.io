---
layout: post
title: maven-agf-plugin - Send a mail for the start of a release
tags: [framework-2-27,maven-codjo-plugin]
---
<u>Context</u>
A mail has to be sent at the beginning of a new framework release build.

<u>Description</u>
The goal ```codjo:send-announcement-to-teams``` has a new parameter ```isStarting```, it can send a mail for the start of a framework release or the end (a starting mail is only sent to subscribers in the Confluence page).

see: http://wp-confluence/confluence/display/framework/maven-codjo-plugin

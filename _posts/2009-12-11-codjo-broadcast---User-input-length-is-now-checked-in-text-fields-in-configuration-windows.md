---
layout: post
title: agf-broadcast - User input length is now checked in text fields in configuration windows
tags: [framework-1-126,codjo-broadcast]
---
<u>Context</u>:
User input length in text fields was not checked in the broadcast configuration windows : data was sometimes truncated in the database.

<u>Description</u>:
Now we are performing a maximum data length checking to limit the users for their data input length.\\
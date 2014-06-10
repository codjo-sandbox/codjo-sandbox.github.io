---
layout: post
title: agf-imports - User input length is now checked in text fields in configuration windows
tags: [framework-1-126,codjo-imports]
---
<u>Context</u>:
User input length in text fields was not checked in the import configuration windows : data was sometimes truncated in the database.

<u>Description</u>:
Now we are performing a maximum data length checking to limit the users for their data input length.
\\
---
layout: post
title: agf-referential - Duplication of line does not work if it contains a primary key field
tags: [framework-1-123,codjo-referential]
---
<u>Context</u>
When duplicating a line of a referential, a form is displayed with all fields pre-filled with values from the duplicated line.

The problem was that all fields taking part of the primary key were not editable. Thus, it was impossible to modify them leading to a "duplicate key" exception when validating the form due to the clash with the duplicated line key.

![Alt attribute text Here](attachments/duplicate.jpg|align=center)

<u>Description</u>
The problem has been fixed. Primary key fields are now editable when duplicating a line of a referential.

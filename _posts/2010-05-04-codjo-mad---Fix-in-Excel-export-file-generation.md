---
layout: post
title: agf-mad - Fix in Excel export file generation
tags: [framework-1-145,codjo-mad]
---
<u>Context</u>:
When executing release tests with an ```assert-excel``` tag, the generated excel file couldn't be closed. A popup message in Excel indicated that the file was already opened.

<u>Description</u>:
In a previous fix to the export file generation, the ```OutputStream``` used to check a generated filename was opened but not closed before returning.

The ```OutputStream``` is now explicitly closed.

See [[codjo-mad - Fix in Excel export file generation|http://wp-confluence.am.agf.fr/confluence/x/JgAGAQ]]
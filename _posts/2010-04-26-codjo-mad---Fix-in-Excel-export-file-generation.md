---
layout: post
title: agf-mad - Fix in Excel export file generation
tags: [framework-1-144,codjo-mad]
---
<u>Context</u>
Some refactoring work has taken place on Excel export actions, which mainly impacted the way file names were generated and used.

Until now, a generated file was considered acceptable for the Excel export action if it was a new (not existing) file, or if the file existed and was in fact a file (as opposed to a directory). 

This caused a problem in two cases:
* release tests expected a particular file, not incrementally generated ones
* if a generated file was opened in Excel and the export action was used again, the previous file would be considered acceptable but could not be written to, and a low-level exception was thrown.

<u>Description</u>
The refactored implementation is now modified to consider opened files while overwriting previously generated unopened files: a generated file is acceptable if it is a writable file. A file cannot be written to if it is opened in Excel, in that case a new file is generated.

See [[codjo-mad - New action SpreadsheetExportAction|http://wp-confluence.am.agf.fr/confluence/x/24f8]]
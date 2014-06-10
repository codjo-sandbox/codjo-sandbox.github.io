---
layout: post
title: agf-mad - Property decimalSeparator in Excel export is not required
tags: [framework-1-169,codjo-mad,hot-topics]
---
<u>Context</u>
The property ```mad.export.excel.decimalSeparator``` was required to parse numbers during an export to Excel.

<u>Description</u>
Now the property is optional. If set, the property must be a **SINGLE CHARACTER**. This single character **IS NOT** a regular expression (_regex_).

For example:
```title=application.properties

See [[codjo-mad - Export Excel]]
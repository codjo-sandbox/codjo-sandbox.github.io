---
layout: post
title: agf-imports - All known field types are displayed in the combo box
tags: [framework-1-181,codjo-imports]
---
<u>Context</u>
When using a quarantine table with a numerical field, the detail view of the corresponding field crashed: it allowed only the "S" (String) field type.

<u>Description</u>
Now all known field types are allowed in the GUI, with a renderer:
* B - Boolean
* C - Class
* D - Date
* N - Numeric
* S - String

Furthermore a check box renderer is used for the "remove left zeros" column.

![Alt attribute text Here](attachments/destFieldType.PNG)
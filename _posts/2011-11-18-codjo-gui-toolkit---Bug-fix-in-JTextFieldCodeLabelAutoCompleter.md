---
layout: post
title: agf-gui-toolkit - Bug fix in JTextFieldCodeLabelAutoCompleter
tags: [framework-2-6-rc1,codjo-gui-toolkit,framework-2-6]
---
<u>Context</u>
When several codes differed only from the case, the wrong one could be selected.

Example:
If the following code-label pair was set :
```
"babar", "un éléphant"
"BABAR", "François Hollande"
"Babar", "Raymond Barre"
```

When the code "babar" was set, searching for the right label was not case-sensitive. Therefore, the "BABAR" code was always found and the same label "François Hollande" was returned even if "babar" or "Babar" codes were set.

```
setCode("babar") displays "François Hollande"
setCode("BABAR") displays "François Hollande"
setCode("Babar") displays "François Hollande"
```

<u>Description</u>
This bug has been fixed.

```
setCode("babar") displays "un éléphant"
setCode("BABAR") displays "François Hollande"
setCode("Babar") displays "Raymond Barre"
```

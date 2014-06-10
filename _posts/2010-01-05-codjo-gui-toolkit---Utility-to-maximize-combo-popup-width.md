---
layout: post
title: agf-gui-toolkit - Utility to maximize combo popup width
tags: [framework-1-128,codjo-gui-toolkit]
---
<u>Context</u>:
In workflow log list screen, combo filters needed to have theirs popups width maximized.

<u>Description</u>:
New class ```ComboBoxPopupWidthMaximizer``` has been created. It allows to configure ```JComboBox``` to have popup displayed maximized, and possibly specify a preferred size for the combo.

<u>Example</u>:
```java
ComboBoxPopupWidthMaximizer.install(myCombo);
...
ComboBoxPopupWidthMaximizer.install(myCombo, 150);
```\\
\\
![Alt attribute text Here](attachments/codjo-gui-toolkit - ComboBoxPopupWidthMaximizer^combo-with-popup-maximized.JPG)\\
\\
see: [[framework:codjo-gui-toolkit - ComboBoxPopupWidthMaximizer]]
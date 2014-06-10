---
layout: post
title: agf-gui-toolkit - Possibility to add an ActionListener to DateField
tags: [framework-1-125,codjo-gui-toolkit]
---
<u>Context</u>:
In order to make ```DateField``` more user friendly and allowing to implement validation by pressing enter key, ```DateField``` had to be modified.

<u>Description</u>:
Methods ```void addActionListener(ActionListener)``` and ```void removeActionListener(ActionListener)``` have been implemented.

<u>Example</u>:
```java
dateField.addActionListener(new ActionListener() {
  public void actionPerformed(ActionEvent e) {
    ...
  }
}

dateField.removeActionListener(myActionListener);
```


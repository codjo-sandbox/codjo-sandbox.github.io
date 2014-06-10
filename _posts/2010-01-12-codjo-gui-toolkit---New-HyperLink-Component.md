---
layout: post
title: agf-gui-toolkit - New HyperLink Component
tags: [framework-1-129,codjo-gui-toolkit,hot-topics]
---
<u>Context</u>:
In Oscar, we needed to display a hypertext-type component.

![Alt attribute text Here](attachments/hyperLink.PNG)

<u>Description</u>:
The class ```HyperLink``` has been added.
When the cursor rolls over, it's replaced with a hand.

<u>Example</u>:

```
      HyperLink hyperLink = new HyperLink("Paramétrage global");

        hyperLink.addActionListener(new ActionListener(){
            public void actionPerformed(ActionEvent e) {
                openPopup();
            }
        });
```

see: [[codjo-gui-toolkit|Utilisation de agf-gui-toolkit]]
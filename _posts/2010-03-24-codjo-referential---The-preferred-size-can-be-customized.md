---
layout: post
title: agf-referential - The preferred size can be customized
tags: [framework-1-139,codjo-referential]
---
<u>Context:</u>
A button has been added to the Smart referential ```RequestToolBar```. Then the default size of the frame became too small to display the 'Rechercher' button.
![Alt attribute text Here](attachments/referential_preferredsize.JPG)



<u>Description:</u>
The ```ReferentialGuiConfiguration``` has been improved. The method ```setPreferredSize``` has been added.
```
public void setPreferredSize(int width, int height)
```

<u>Example:</u>
```
// default widht = 1000
// default height = 600
referentialGuiPlugin.getConfiguration().setPreferredSize(1000,600);
```

see: [[framework:codjo-referential - How to define the preferred size of the referential frame]]

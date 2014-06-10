---
layout: post
title: agf-referential - Fix sort order on referential family GUI
tags: [framework-1-149,codjo-referential]
---
<u>Context:</u>
The GUI is composed of the family list, and the two lists from the ```SelectionGui``` : a referential list and an association list.
- On the referential list, sorting was enabled on the header of the list, but not working properly,
- On the association list, when modifying its content, sorting was not woking properly.

<u>Description:</u>
- Now, it is not possible anymore to sort the referential list using&nbsp;its header. The list has always the same sort order,
- Moreover, the association list has always the same sort order.

<u>Example:</u> ![Alt attribute text Here](attachments/ref-family.jpg)
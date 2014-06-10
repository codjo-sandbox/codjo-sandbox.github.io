---
layout: post
title: agf-release-test - ClickRight on JComboBox
tags: [hot-topics,framework-1-126,codjo-release-test]
---
<u>Context</u>:
We have to test the Right Click on a JComboBox which should make appear a Popup Menu.

<u>Description</u>:
The step ```ClickRightStep``` accepts now to manage ```JComboBox```. 

<u>Example</u>: 
```
<clickRight name="myCombo" popupVisible="true" row="1" select="Modify value"/>
```
This action performs a right click on the second item of the combobox, and select the menu "Modify value".

see: [[codjo-release-test|http://wp-confluence/confluence/display/framework/agf-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-clickRight]]
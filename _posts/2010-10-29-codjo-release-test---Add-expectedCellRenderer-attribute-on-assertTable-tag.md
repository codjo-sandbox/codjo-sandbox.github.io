---
layout: post
title: agf-release-test - Add expectedCellRenderer attribute on assertTable tag
tags: [framework-1-172,codjo-release-test]
---
<u>Context</u>:
On Mint application, we needed to test if a table cell uses a particular renderer.

<u>Description</u>:
The ```expectedCellRenderer``` attribute is added on ```assertTable``` tag.

<u>Example</u>:

```language=xml|title=Release test file
...
<assertTable name="wip" row="0" expected="5.23" 
            column="Limite inférieure" mode="model" 
            expectedCellRenderer ="com.agf.mint.gui.product.changes.synthesis.MultiValueChangeRenderer"/>
        
...
```
---
layout: post
title: agf-mad - Change type of listener on FilterPanel
tags: [framework-1-145,codjo-mad]
---
<u>Context</u>
The intialization of the ```RequestComboBox``` on a ```FilterPanel``` with an automatic search is very long.

<u>Description</u>
Each time a comboBox is added to the ```FilterPanel``` the filtering is executed on the data load of each comboBox, it's the cause of long time initializing.
The ```ActionListener``` is replaced by an ```ItemActionListener``` that execute the search event when a selection is made on a comboBox.

See: [[framework:codjo-mad - Utilisation#filterpanel]]
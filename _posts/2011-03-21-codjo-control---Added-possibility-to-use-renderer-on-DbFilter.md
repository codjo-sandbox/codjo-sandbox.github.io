---
layout: post
title: agf-control - Added possibility to use renderer on DbFilter
tags: [framework-1-191,codjo-control]
---
<u>Context</u>
It was impossible to use renderer on ```DbFilter```.

<u>Description</u>
To use renderer on DbFilter, set the ```renderer``` attribute in your ```quarantine.xml``` file :

```
<quarantines>
    <gui name="My quarantine table">
        <window>
            <dbFilter renderer="com.agf.orbis2.gui.controls.quotation.ErrorCodeRenderer">errorType</dbFilter>
      ...
        </window>
    </gui>
</quarantines>
```

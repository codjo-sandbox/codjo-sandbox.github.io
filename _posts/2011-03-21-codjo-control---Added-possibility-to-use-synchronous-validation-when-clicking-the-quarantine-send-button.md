---
layout: post
title: agf-control - Added possibility to use synchronous validation when clicking the quarantine send button
tags: [framework-1-191,codjo-control]
---
<u>Context</u>
We want to use synchronous validation after clicking the send button.
We do not want users still click on the "Envoyer" button until all treatments are performed.

<u>Description</u>
To use synchronous validation, set the ```syncValidation``` attribute in your ```quarantine.xml``` file as the example below :

```
<quarantines>
    <gui name="My quarantine table">
        <window syncValidation="true">
          ...
          ...
        </window>
    </gui>
</quarantines>
```

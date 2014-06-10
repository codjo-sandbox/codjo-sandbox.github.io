---
layout: post
title: agf-tokio - Bug with "group" tag name
tags: [framework-1-137,codjo-tokio]
---
<u>Context</u>:
Currently, the ```<group>``` tags are removed at parsing time.
By side effect, all the tags starting with "group" are removed.

For example, in this case: 

```
<group>
  <GPT_ap_gui_preferences>
    <row>
      <group_name value="LAL_Portefeuille"/>
    </row>
    ...
  </GPT_ap_gui_preferences>
</group>
```

... the "group_name" column is lost.

<u>Description</u>:
The parser has been corrected. It removes only the relevant tag.
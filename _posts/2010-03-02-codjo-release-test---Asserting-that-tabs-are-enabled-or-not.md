---
layout: post
title: agf-release-test - Asserting that tabs are enabled or not
tags: [framework-1-136,codjo-release-test,hot-topics]
---
<u>Context:</u>
In Damas project, some screen have got some tabbed pane with disabled tabs. It was needed to test the disabled tabs.

<u>Description:</u>
The "enabled" parameter was added to "assertTab" tag. By now, using this parameter, it's possible to test if a tab is enabled or not.

```xml
  <assertTab name="myTabbedPane" tabLabel="myTab" enabled="false" />
```

see : [[framework:codjo-release-test - Tags IHM#assertTab]]


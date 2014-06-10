---
layout: post
title: agf-imports - Possibility to not truncate imported file names
tags: [framework-2-13,codjo-imports,hot-topics]
---
<u>Context</u>
Names of imported files were truncated with the 30 latest characters.

<u>Description</u>
Add method ```setTruncateFileName(boolean)``` to ```ImportServerPluginConfiguration``` interface in order to truncate or not the file names. By default the behaviour stills the same as before (the file names will be truncated).
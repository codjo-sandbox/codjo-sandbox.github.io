---
layout: post
title: agf-broadcast - Internationalization of GUI components (part 2)
tags: [framework-1-184,codjo-broadcast]
---
<u>Context</u>
Applications need to be internationalized. Therefore, all framework libraries that expose GUI components or contain messages dedicated to the user have to be internationalized too.

<u>Description</u>
Some GUI components have been internationalized. A ```BroadcastGuiContext``` class has been created to facilitate unitary tests. This class loads automatically i18n properties related to this library.
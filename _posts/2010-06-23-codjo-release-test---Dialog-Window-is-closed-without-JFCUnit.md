---
layout: post
title: agf-release-test - Dialog Window is closed without JFCUnit
tags: [framework-1-152,codjo-release-test]
---
<u>Context</u>
We had an exception when we closed the dialog window when the release test is finished.

<u>Descriptif</u>
JFCUnit methods to close the dialog window don't work correctly, so we call the methods ```setVisible``` and ```dispose``` on the dialog window.
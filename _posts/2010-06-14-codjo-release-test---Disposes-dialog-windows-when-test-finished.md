---
layout: post
title: agf-release-test - Disposes dialog windows when test finished
tags: [codjo-release-test,framework-1-151]
---
<u>Context</u>:
When a release test is finished with an error showing in a ```JDialog```, other release tests are impacted because the dialog is still visible.

<u>Description</u>:
Now when we clear the main window at the end of the test, we dispose remaining dialogs.

[[codjo-release-test - Dialog Window is closed without JFCUnit | http://wp-confluence.am.agf.fr/confluence/x/ngMbAQ]]


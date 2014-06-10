---
layout: post
title: agf-security - Hide login window while SplashScreen is shown
tags: [framework-1-194,codjo-security]
---
<u>Context</u>
During login phase, splashscreen is shown and the login window is still accessible.

<u>Description</u>
Now the window is hidden as long as splashscreen is visible. 

When an error occurs during login phase (bad login or lack of authorisation), an error message is displayed and the user is redirected to the login window.

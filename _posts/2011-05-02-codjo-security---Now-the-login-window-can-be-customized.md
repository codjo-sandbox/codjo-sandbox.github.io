---
layout: post
title: agf-security - Now the login window can be customized
tags: [framework-1-196,codjo-security]
---
<u>Context</u>
In order to remove duplicated code between Benchmark and Framework, we need to modify some framework libraries.

<u>Description</u>
Now, the login window can be customized with an extra component. This component is added at the bottom of the window. 

<u>Example</u>
```
   securityGuiPlugin.getConfiguration()
                    .setLoginExtraComponent(new JTextField("my extra component"));
```

![Alt attribute text Here](attachments/login-with-extraComponent.png|thumbnail,align=center)
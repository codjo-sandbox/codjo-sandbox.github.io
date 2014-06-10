---
layout: post
title: agf-mad - Add the possibility to remove a session component
tags: [framework-1-196,codjo-mad]
---
<u>Context</u>
In order to remove duplicated code between Benchmark and Framework, we need to modify some framework libraries.

see : [[framework:/2011/05/02/codjo-control - Implement the stop of the control server plugin]]

<u>Description</u>
To be able to do some clean-up (for example in the ```ControlServerPlugin```), we add the possibility to remove session component (```removeSessionComponent``` method).

<u>Example</u>
```
    madServerPlugin.getConfiguration()
                   .removeSessionComponent(MyComponent.class);
```

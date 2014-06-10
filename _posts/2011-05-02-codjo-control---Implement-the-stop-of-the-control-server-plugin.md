---
layout: post
title: agf-control - Implement the stop of the control server plugin
tags: [framework-1-196,codjo-control]
---
<u>Context</u>
In order to remove duplicated code between Benchmark and Framework, we need to modify some framework libraries.

see : [[framework:/2011/05/02/codjo-mad - Add the possibility to remove a session component]]

<u>Description</u>
Starting now, the ```ControlServerPlugin``` will do the necessary clean-up during the stop cycle.

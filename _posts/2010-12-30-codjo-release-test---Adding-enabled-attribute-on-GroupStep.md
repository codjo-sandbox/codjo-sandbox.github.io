---
layout: post
title: agf-release-test - Adding enabled attribute on GroupStep
tags: [framework-1-181,codjo-release-test,hot-topics]
---
<u>Context</u>:
xmf files lacks of&nbsp;flexiblity and needs a system for deactivating group.

<u>Description</u>:
A new attribute ```enabled``` has been added on tag ```group```.
If this attribute is provided with the value "false", all steps inside this group will be ignored.


<u>Example</u>:
example.xml:

```
 <call-method file="example.xmf">
  <parameter name="assertFrame" value="false"/>
 </call-method>
```

example.xmf:
```
<group name="groupe qui teste l'existence d'une frame" enabled="@assertFrame@">
 <assertFrame title="fenetre"/>
</group>
```

In this example, the parameter ```assertFrame``` is provided with ```"false"``` value. So, the ```assertFrame``` isn't asserted in the xmf file.


see : [[doc|http://wp-confluence/confluence/display/framework/codjo-release-test<u>-</u>Tags+IHM#agf-release-test-TagsIHM-group]]
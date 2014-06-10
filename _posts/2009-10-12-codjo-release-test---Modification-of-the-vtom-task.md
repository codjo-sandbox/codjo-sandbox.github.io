---
layout: post
title: agf-release-test - Modification of the vtom task
tags: [framework-1-117,codjo-release-test]
---
The properties in the ```line``` attribute of the ```arg``` sub-tag are now replaced.

**e.g**: if you have the property ```my.option``` with the value ```toto```
and the following release test fragment:

```xml
<vtom ...>
    <arg line="-opt ${my.option}"/>
</vtom>
```

will be expanded as
```xml
<arg line="-opt toto"/>
```

cf. tag documentation : [[vtom]]
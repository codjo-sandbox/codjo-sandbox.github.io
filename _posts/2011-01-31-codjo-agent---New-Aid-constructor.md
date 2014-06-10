---
layout: post
title: agf-agent - New Aid constructor
tags: [framework-1-185,codjo-agent]
---
<u>Context</u>
Writing unit tests with agents, we find the API for creating Aid not very clear (not easy to read).

<u>Description</u>
The second parameter of the constructor was a boolean, it has been transformed in an ```enum``` (the previous constructor still exists but is deprecated).

```
    public enum NameType {
        // john@host:8080/JADE
        GLOBAL,
        // john
        LOCAL
    }
```

<u>Example</u>
```
    String name="john@host:8080/JADE";
    ...
    new Aid(name, false)

Can be replaced by
    String name="john@host:8080/JADE";
    ...
    new Aid(name, NameType.GLOBAL) 
```



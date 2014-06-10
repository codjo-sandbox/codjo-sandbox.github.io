---
layout: post
title: agf-test - Bug fix on LogString
tags: [framework-1-140,codjo-test]
---
<u>Context:</u>
The following method upon ```LogString```

```
public void call(String methodName, Object... parameters);
```

raised an exception if no parameter was given.

<u>Description:</u>
This bug has been fixed.

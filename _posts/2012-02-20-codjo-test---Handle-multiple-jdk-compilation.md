---
layout: post
title: agf-test - Handle multiple jdk compilation
tags: [framework-2-15,codjo-test]
---
<u>Github</u>

see :[[Pull request|https://github.com/codjo/codjo-test/pull/1]]

<u>API change</u>
```
//Before
ResultSet rs = new ResultSetMock();
....

//Now
ResultSet rs = new ResultSetMock().getStub();

```

<u>Application Impact</u>
* Magic
* Roses

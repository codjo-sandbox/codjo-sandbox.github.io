---
layout: post
title: agf-tokio - Change in timestamp comparison
tags: [framework-1-119,codjo-tokio]
---
Due to the future jconnect upgrade, timestamp management in tokio has to be changed.

Now, when tokio compares timestamps, it keeps a precision of 10 milliseconds.

<u>Example</u>: In the following example, the date used in comparison will be ```2000-04-06 17:58:25.12```

```xml
<myTtable>
  <row>
    ..
    <FIRST_VALUATION_DATE value="2000-04-06 17:58:25.123456789"/>
    ..
  </row>
</myTtable>
```
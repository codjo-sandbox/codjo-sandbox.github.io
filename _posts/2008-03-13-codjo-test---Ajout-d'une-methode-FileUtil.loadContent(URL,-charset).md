---
layout: post
title: agf-test - Ajout d'une méthode FileUtil.loadContent(URL, charset)
tags: [codjo-test,framework-1-35]
---
Enrichissement de FileUtil pour proposer une signature sur loadContent prenant une URL et un type d'encodage ("UTF-8", "UTF-16", etc.).

L'API sur loadContent est la suivante :

```
public static String loadContent(Reader reader) throws IOException;
public static String loadContent(File file) throws IOException;
public static String loadContent(URL url) throws IOException;
public static String loadContent(URL url, String charset) throws IOException;
```


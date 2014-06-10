---
layout: post
title: agf-test - Correction de l'assert avec ellipses
tags: [framework-1-115,codjo-test]
---
Dans la classe ```LogString```, les méthodes ```assertContent(String...)``` et ```assertAndClear(String...)``` coupaient les logs d'appels de méthode ayant une liste d'arguments. Ce problème est corrigé, les méthodes avec arguments sont bien considérées comme une seule chaîne.

**AVANT**
```
logString.call("foo", "pim", "pam", "poum");
[[...]]
logString.assertContent("foo(pim",
                        "pam",
                        "poum)");
```

**APRES**
```
logString.call("foo", "pim", "pam", "poum");
[[...]]
logString.assertContent("foo(pim, pam, poum)");
```


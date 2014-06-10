---
layout: post
title: agf-datagen - Requetor is now available in quarantines
tags: [framework-2-8,codjo-datagen]
---
<u>Context</u>
```RED``` needed to offer the requetor service to users on quarantine tables. The ```user-quarantine``` xml tag that was responsible for generating automatically handlers linked to the quarantine did not manage the requetor handler.

<u>Description</u>
The ```user-quarantine``` xml tag allows now to generate the requetor handler. By default, this handler is not generated. The ```requetor``` attribute must be set to ```true``` to generate the handler, as follows:

```
<user-quarantine requetor="true" 
                 name="com.agf.mint.data.QUserPerformanceBench"
                 table="Q_AP_USER_PERFORMANCE_BENCH"/>
```
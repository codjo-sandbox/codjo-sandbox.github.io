---
layout: post
title: agf-segmentation - ExpressionCompilerCommand modified due to API change in QueryConfig
tags: [framework-1-175,codjo-segmentation,api-change,codjo-sql]
---
<u>Context</u>
Due to API change in ```QueryConfig``` (```codjo-sql```), ```ExpressionCompilerCommand``` does not compile (see: [[framework:/2010/11/19/agf-sql - Order by fields can be defined when generating Select queries]]).

<u>Description</u>
It has been fixed.
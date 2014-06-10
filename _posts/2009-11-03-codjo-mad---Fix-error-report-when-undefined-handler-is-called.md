---
layout: post
title: agf-mad - Fix error report when undefined handler is called
tags: [framework-1-120,codjo-mad]
---
When an undefined ```handler``` was called, an unexpected ```ClassCastException``` was thrown during the creation of the error report. 

Now the error message is correctly built.

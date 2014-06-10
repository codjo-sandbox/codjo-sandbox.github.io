---
layout: post
title: agf-release-test - AssertExcel task retries even if a JComException is thrown
tags: [framework-1-122,codjo-release-test]
---
<u>Context</u>
The task ```assertExcel``` fails if the method ```applicationManager.WorkBooks()``` throws a ```JComException```.

<u>Description</u>
The ```JComException``` is catched and logged, and the task retries with the principle described here : [[framework:/2009/07/15/codjo-release-test - Tentative multiple pour la comparaison Excel]].
---
layout: post
title: agf-referential - API change in ReferentialGui and ReferentialAssoForm
tags: [framework-1-149,codjo-referential,api-change]
---
<u>Context:</u>
In ```ReferentialGui``` and ```ReferentialAssoForm``` some getters were not used, and some others had a too wide visibility.

<u>Description:</u>
- In ```ReferentialGui```, the following public getters have been removed : ```getSearchField```, ```getResetSearchButton``` and ```getTreeFilterModel```
- In ```ReferentialAssoForm```, ```getMainPanel``` has been removed.  The visibility of the following getters has been narrowed to ```package``` : ```getSelectionGui```, ```getFamilyList``` and ```getOkButton```







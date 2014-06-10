---
layout: post
title: agf-security - New CSV role export available
tags: [framework-1-170,codjo-security,hot-topics,framework-1-170-1]
---
<u>Context</u>:
```mint``` security model intensely uses composite roles. Thus, it has become difficult to have a good overview of roles dependencies.

<u>Description</u>:
A new CSV export has been made. It figures relationship between roles like this:
<table>
<tr>
<th></th><th>functionRole1</th><th>functionRole2</th><th>userRole1</th><th>userRole2</th></tr>
<tr>
<td> functionRole1 </td>
<td> 1 </td>
</tr>
<tr>
<td> functionRole2 </td>
<td> 1 </td>
</tr>
<tr>
<td> unitRole1 </td>
<td> 1 </td>
<td> 2 (functionRole1) </td>
</tr>
<tr>
<td> unitRole2 </td>
<td> 1 </td>
<td> 2 (functionRole2)</td>
</tr>
<tr>
<td> unitRole3 </td>
<td> 1 </td>
</tr>
</table>

In this example, ```userRole1```, ```userRole2```, ```functionRole1``` and ```functionRole2``` are composite roles, ```unitRole1```, ```unitRole2``` and ```unitRole3``` are simple roles.
We have following relationships:
* ```functionRole1``` contains ```unitRole1```,
* ```functionRole2``` contains ```unitRole2```,
* ```userRole1``` contains ```functionRole1```, ```unitRole3``` and transitively ```unitRole1```,
* ```userRole2``` contains ```functionRole2``` and transitively ```unitRole2```.

see: [[framework:Guide Utilisateur IHM de codjo-security common]]
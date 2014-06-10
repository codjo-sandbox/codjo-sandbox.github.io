---
layout: post
title: agf-pom - user_tr and user_dev properties moved to super-pom
tags: [hot-topics,framework-1-151,codjo-pom]
---
<u>Context</u>:
user_tr and user_dev passwords have to be changed, moving it to the super-pom will decrease the amount of work each time we have to change it.

<u>Description</u>:
Properties ```defaultUser```, ```defaultUserPassword```, ```defaultTestUser```, ```defaultTestUserPassword```, ```batchUserLogin``` and ```batchUserPassword``` have been moved to the super-pom


<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
these properties have to be removed from applications' pom
</p></td>
          </tr>
</table>

---
layout: post
title: agf-workflow - Server configuration updated to register JobFilter
tags: [framework-1-165,codjo-workflow]
---
<u>Context</u>
ROSES needs to hide some workflow types from the task manager window and from the workflow log window.

<u>Description</u>
It is now possible to configure the ```WorkflowServerPlugin``` to register a new ```JobFilter```.
```
    workflowServerPlugin.getConfiguration().registerJobFilter(new NotificationFilter());
```


<table style='background-color: #FFFFCE;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/warning.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
Be careful when extending the ```JobFilter``` class: do not forget to call the next filter's methods
```
    @Override
    public boolean filter(JobRequest jobRequest) {
        return NotificationRequest.NOTIFY_JOB_TYPE.equals(jobRequest.getType())
               || (null != nextFilter && nextFilter.filter(jobRequest));
    }
```
</p></td>
          </tr>
</table>


See [[codjo-workflow - Using JobFilter to filter out some Job or JobRequest]]
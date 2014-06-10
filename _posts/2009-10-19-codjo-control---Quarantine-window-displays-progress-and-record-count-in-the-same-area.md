---
layout: post
title: agf-control - Quarantine window displays progress and record count in the same area
tags: [framework-1-118,codjo-control]
---
The ```DefaultQuarantineWindow``` displayed both a ```ProgressBarLabel``` and a ```RequestToolBar``` in its bottom part, even if only one of the two components would be useful at any time:
- either the ```ProgressBarLabel``` when a task was running in the background, such as moving records from a quarantine table to the user's copy
- or the ```RequestRecordCoundField``` of the ```RequestToolBar``` displaying the total number of lines in the table and the number of lines in the user's view.

The ```DefaultQuarantineWindow``` now uses the [[new ```RequestToolBar``` API|http://wp-confluence/confluence/x/a4DO]] to put its ```ProgressBarLabel``` in place of the ```RequestRecordCountField``` at initialization, and put back the ```RequestRecordCountField``` when the quarantine table is loaded. Screen captures below.

{panel:title=When loading table}
![Alt attribute text Here](attachments/quarantinewindow3.PNG)
{panel}
\\
{panel:title=After table is loaded}
![Alt attribute text Here](attachments/quarantinewindow4.PNG)
{panel}
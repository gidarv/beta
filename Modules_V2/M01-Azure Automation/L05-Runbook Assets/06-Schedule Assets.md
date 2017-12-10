# Schedule Assets  

Many times, you want the scripts to self-trigger at certain times of the day. The [Automation schedule](https://azure.microsoft.com/en-us/documentation/articles/automation-schedules/) functionality gives you the ability to set up schedules for an execution. It supports both single-trigger and multi-trigger schedules. A runbook can be linked to multiple schedules, and a schedule can have multiple runbooks linked to it.

Here is a schedule that runs every night at midnight. To retrieve the schedule use the Azure PowerShell command [Get-AzureRmAutomationSchedule](https://msdn.microsoft.com/en-us/library/mt603733.aspx).

![](../../Linked_Image_Files/1.4.3.png)

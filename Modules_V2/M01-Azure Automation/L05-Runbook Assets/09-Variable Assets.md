# Variable Assets  


<table width="103%">
<tbody>
<tr>
<td width="45%">



           ![]( ../../Linked_Image_Files/1.4.6.png)

</td>
<td width="53%">


[Variable assets](https://azure.microsoft.com/en-us/documentation/articles/automation-variables/) are persistent values that are available to all runbooks and DSC configurations in your automation account. Variables can be String, Boolean, DateTime, Integer, or Not Specified.

Variable assets can be encrypted along with credentials, certificates, and connections assets. These assets are encrypted and stored in Azure Automation by using a unique key that is generated for each Automation account.

To retrieve an unencrypted variable, use the [Get-AzureAutomationVariable](http://msdn.microsoft.com/library/dn913772.aspx) command. To retrieve any encryption assets, use a **Get-AutomationVariable** activity in a runbook or DSC configuration.

</td>
</tr>
</tbody>
</table>


Automation variables are useful for:

- Sharing a value among multiple runbooks or DSC configurations.

- Sharing a value among multiple jobs from the same runbook or DSC configuration.

- Managing a value from the portal or from the Windows PowerShell command line that is used by runbooks or DSC configurations, such as a set of common configuration items like a specific list of virtual machine (VM) names, a specific resource group, or an Active Directory domain name.

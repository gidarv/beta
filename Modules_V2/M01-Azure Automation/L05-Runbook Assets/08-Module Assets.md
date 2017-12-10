****# Module Assets

A PowerShell module is a set of related Windows PowerShell functionalities, grouped together as a convenient unit. PowerShell modules can be imported as needed, and are often installed with a particular feature. For example, if you add the Active Directory role to your server, the Active Directory PowerShell module with all the associated cmdlets will also be installed.

An Azure module asset isn't very different from a PowerShell module. It's simply a PowerShell module that optionally contains one additional file - a metadata file specifying an Azure Automation connection type to be used with the module. For example, email modules typically include a connection type. Azure module assets can be imported to make their cmdlets available for use within runbooks and DSC configurations.

Certain module assets are shipped as “global module assets” in the Automation service. These global modules are available to you when you create an Automation account. Notice in the graphic Azure.Storage, AzureRM.Automation, and AzureRM.Compute. You can add additional modules by browsing the gallery.

![Screenshot of Module Gallery](/static/1.4.5.png)

<table border="0" cellpadding="0">
<tbody>
<tr>
<td width="15%">

![Checkmark]( ../../Linked_Image_Files/checkmark.png)

</td>
<td>To retrieve a module, use the [Get-AzureRmAutomationModule](https://msdn.microsoft.com/en-us/library/mt603711.aspx) command.</td>
</tr>
</tbody>
</table>
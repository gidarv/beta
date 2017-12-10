# Credential Assets  

An Automation [credential asset](https://azure.microsoft.com/en-us/documentation/articles/automation-credentials/) holds a **PSCredential** object that contains security credentials. For example, credentials could be your Microsoft Azure login username and password. Runbooks and DSC configurations can use the [Get-AzureAutomationCredential](https://msdn.microsoft.com/en-us/library/mt619436.aspx) cmdlet to authenticate applications and services. 

![](../../Linked_Image_Files/1.4.2.png)

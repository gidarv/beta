# Connection Assets

[Connection assets](https://azure.microsoft.com/en-us/documentation/articles/automation-connections/) define the information required to connect to a service or application. The different types of connections that you can create are defined by the modules imported into Azure Automation.

![]( ../../Linked_Image_Files/1.4.7.png)

After you select the connection type, a template that defines the properties needed by the connection will display. For example, the Azure module that comes preinstalled in Azure Automation contains a connection with fields for subscription ID and certificate, which is the information needed to manage your Azure resources programmatically. For example, the **SMTPServerConnection** type shows properties associated with email server connections.

![]( ../../Linked_Image_Files/1.4.8.png)

The properties for a connection are stored securely in Azure Automation and can be accessed in the runbook with the **Get-AutomationConnection** activity. 

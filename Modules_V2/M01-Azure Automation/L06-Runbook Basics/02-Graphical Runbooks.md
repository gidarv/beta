# Graphical Runbooks  

[Graphical runbooks](https://azure.microsoft.com/en-gb/documentation/articles/automation-graphical-authoring-intro/) allow you to create runbooks for Azure Automation without the complexities of the underlying Windows PowerShell or PowerShell Workflow code. You create your workflow by adding activities from the library, linking them together, and then configuring the components.

Graphical and graphical PowerShell Workflow runbooks are created and edited with the graphical editor in the Azure portal. You can export them to a file and then import them into another automation account, but you cannot create or edit them with another tool. Graphical runbooks generate PowerShell code, but you can't directly view or modify the code. Graphical runbooks cannot be converted to one of the text formats, nor can a text runbook be converted to graphical format. Graphical runbooks can be converted to graphical PowerShell Workflow runbooks during import and vice versa.

![]( ../../Linked_Image_Files//1.5.2.png)

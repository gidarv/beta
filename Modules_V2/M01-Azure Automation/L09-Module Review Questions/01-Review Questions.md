## 1. Drop-down
<<display_name:DevOps200_2.01.001_DR; max_attempts:2; showanswer:finished; weight:2.0>>
You are automating your company’s infrastructure.   
You need to create the appropriate Azure resources.   
Which two steps must you perform?  
Step 1. Create an Azure subscription with the following role:   
[[  
Automation Operator  
Contributor  
(Owner)  
Reader  
Security Manager  
]]  
Step 2. Use the subscription to create the following type of account:  
[[  
Active Directory  
(Automation)  
Integration  
Storage  
]]  
[explanation]   
You must create an Azure subscription with the owner role. The owner role is required because it has the privileges needed to create the appropriate automation resources. None of the other roles have sufficient privileges to create an Azure Automation account. You must also create an Azure Automation account. This account will be used to contain the relevant objects, including Automation runbooks.  
[explanation] 

---
## 2. Multiple choice
<<display_name:DevOps200_2.01.002_MC; max_attempts:2; showanswer:finished; weight:1.0>>

You manage Azure resources for a company.  
You need to ensure that the administrators can assign and modify permissions and roles but cannot modify any Automation resources.   
Which role should you assign to each user?  

(!) Automation operator  
( ) Contributor  
( ) Owner  
( ) Reader  
(x) User access administrator  

[explanation]  
The correct answer is User access administrator. Users with this role can manage the access of other users but cannot perform any other actions. Contributor, Reader, and Automation operator roles do not grant the privilege to manage permissions and roles, while Owner grants too many privileges.  
[explanation]  
---
## 3. Numerical input
<<display_name:DevOps200_2.01.003_NI  ; max_attempts:2; showanswer:finished; weight:1.0>>
Your application pipeline includes three main areas: Development, staging, and production. In addition, you have two operational groups: Western division and Eastern division.   
How many Azure Automation accounts should you create? Enter a whole number that represents the number of accounts to create.
=6  
[explanation]   
The correct answer is 6. This is because the best strategy is to use multiple Automation accounts, segregating the accounts based on functional groups. For each division, you create one Automation account each for development, staging, and production. You should not use a single Automation account because this would greatly increase the complexity of the solution and increase exposure and risk.   
[explanation]   
---
## 4. Drop-down
<<display_name:DevOps200_2.01.004_DR; max_attempts:2; showanswer:finished; weight:2.0>>

What do you use to authenticate Automation runbooks?  
[[  
administrator account  
authorization token  
(certificate)  
username and password  
]]  
What do automation runbooks inherit their role from?  
[[  
active user account  
administrator account  
(service principle)  
subscriber account  
]]  
[explanation]  
Runbooks are authenticated by using a certificate. The certificate authenticates against a service principal. The service principal acts as a proxy account. It is a special Azure Active Directory account that is set up for authentication but does not belong to a person.    
[explanation]  
---
## 5. Check box
<<display_name:DevOps200_2.01.005_CB; max_attempts:2; showanswer:finished; weight:3.0>>

Your company has on-premises datacenters in six regions around the world. Each datacenter has Microsoft SQL Server instances that support a business application.  
You need to automatically truncate database log files for all Microsoft SQL Server instances each day.  
Which three automation resources should you implement?  

[X] connection asset  
[X] hybrid runbook  
[ ] runbook  
[X] scheduling asset  
[ ] variable asset 

[explanation]  
To automate on-premises assets such as an on-premises SQL Server database, you must use a hybrid workbook. A standard runbook can only automate Azure resources. The hybrid workbook is stored on Azure, but when it runs, it is copied to the on-premises server so that it has access to on-premises resources. At a minimum, the hybrid runbook must contain a scheduling asset to trigger the hybrid runbook to run each day, and a connection asset to connect to the required SQL Server database.  
[explanation]  
---
## 6. Drop-down
<<display_name:DevOps200_2.01.006_DR; max_attempts:2; showanswer:finished; weight:2.0>>
You are developing an Azure application by using Visual Studio. The application must allocate Azure resources based on various criteria, including current resource utilization and current resource budgets.  
The application must use a:  
[[  
runbook  
(webhook)  
]]  
The application must trigger a:  
[[  
(runbook)  
webhook  
]]  
[explanation]  
Each time the criteria are met to allocate a resource, the application must use a webhook to trigger the appropriate runbook. A webhook is a resource that is set up in Azure and is configured to run a runbook. The webhook is triggered by using an HTTPS call that can be generated by the application.  
[explanation]  
---
## 7. Drop-down
<<display_name:DevOps200_2.01.007_DR ; max_attempts:2; showanswer:finished; weight:1.0>>

You develop an Azure solution for an energy company. The solution uses an Azure Resource Manager virtual machine named ECDataServer for data processing. You must shut down ECDataServer after each processing cycle completes to minimize costs. You must configure the shutdown by using Azure Automation.  
Which Azure PowerShell command should you run?   
[[  
(Stop-AzureRmVM -Name ECDataServer -ResourceGroupName ECRG -Force)  
Stop-AzureRmVM -Name ECDataServer -ResourceGroupName ECRG -Force -StayProvisioned  
Stop-AzureVM -ServiceName "ECRG" -Name "ECDataServer" -Force  
Stop-AzureVM -ServiceName "ECRG" -Name "ECDataServer"  
]]  

[explanation]  
The <b>Stop-AzureRmVR</b> PowerShell command can only be used to stop an Azure ARM virtual machine. The <b>–Force</b> parameter can be used to bypass any message prompt that might appear and prevent Automation from running the script. The <b>–StayProvisioned</b> parameter is not used to stop compute charges on the virtual machine.  
[explanation]  
---
## 8. Multiple choice
<<display_name:DevOps200_2.01.008_MC; max_attempts:2; showanswer:finished; weight:1.0>>
You have a Windows PowerShell script that contains a series of commands.  
You must ensure that all of the commands run concurrently.  
Which property should you add to the top of the script?
( )Threaded  
(x)Parallel  
( )Multiple  
( )Concurrent  

[explanation]  
The Parallel property can be used in a cmdlet to run multiple commands concurrently instead of sequentially, as with a typical script.  
[explanation]  
---
## 9. Check Box
<<display_name:DevOps200_2.01.009_CB; max_attempts:2; showanswer:finished; weight:1.0>>
You develop an Azure solution that includes multiple virtual machines (VMs) that are managed by a runbook. The VMs work concurrently to process complex geospatial data. The VMs send a RESTful push when they complete processing.  
You need to respond to the REST calls.   
What should you implement?  
[ ]Azure API  
[ ]Runbook  
[ ]Service Bus queue  
[x]Webhook  

[explanation]  
A webhook can be used to respond to RESTful calls.  
[explanation]  
---
## 10. Drop-down
<<display_name:DevOps200_2.01.010_DR; max_attempts:2; showanswer:finished; weight:1.0>>
You develop an Azure solution that includes a 3D graphics application that runs in a virtual machine. The application requires authentication to Azure resources.  
Which Azure PowerShell command should you use?   
[[  
Get-AutomationCertificate  
(Get-AutomationPSCredential)  
Get-AzureRmVM  
Get-AzureAccount  
]]  

[explanation]  
The Get-AutomationPSCredential command is used to access the PSCredential that is part of a certificate. This is required to authenticate the application.  
[explanation]  
---
## 11. Multiple choice
<<display_name:DevOps200_2.01.011_MC ; max_attempts:2; showanswer:finished; weight:1.0>>
You develop an Azure solution that includes multiple virtual machines (VMs) that are managed by a runbook. The VMs work concurrently to process complex geospatial data. The VMs send a RESTful push message when they complete processing.  
You need to respond to the REST calls.  
What should you implement?  
(!)Azure API  
( )Runbook  
( )Service Bus queue  
(x)Webhook  

[explanation]   
A webhook can be used to respond to RESTful calls.  
[explanation]  
---
## 12. Multiple choice
<<display_name:DevOps200_2.01.012_MC ; max_attempts:2; showanswer:finished; weight:1.0>>
You manage an Azure environment. You hire a new administrator named User1.  
User1 must be able to create Azure Run As accounts.  
Which role should you assign to User1?  
(!)Contributor  
(x)Owner  
( )Reader  
( )Security Manager  

[explanation]  
The ownwer role is able to configure Run As accounts.  
[explanation]  
---
## 13. Multiple choice
<<display_name:DevOps200_2.01.013_MC ; max_attempts:2; showanswer:finished; weight:1.0>>
You manage an Azure environment. You plan to implement state management.  
You need to be able to perform backups of non-database systems.  
What should you create?  
(!)Storage account  
(x)Run As account  
( )Runbooks  
( )Webhooks  

[explanation]  
To use an Automation account as required to perform these tasks, a Run As account must be specified.  
[explanation]  
---
## 14. Check box
<<display_name:DevOps200_2.01.014_CB; max_attempts:2; showanswer:finished; weight:2.0>>

You manage an Azure environment. A User named User1 must be able to create, modify, and run runbooks in Azure.  

Which two roles can you assign to User1?  

[]Automation Operator  
[x]Contributor  
[x]Owner  
[]Reader  
[]User access administrator  

[explanation]  
Owners and contributors can create and modify runbooks. Automation operators can only start runbooks.   
[explanation]  
---
## 15. Multiple choice
<<display_name:DevOps200_2.01.015_MC; max_attempts:2; showanswer:finished; weight:1.0>>

You need to share a value between Azure automation runbooks.  
What should you use?  

(!)Connection asset  
(x)Variable asset  
()Certificate asset  
()Module asset  

[explanation]  
Variable assets can be defined and encrypted, and can be used across runbooks.  
[explanation]  

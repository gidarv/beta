# Webhooks  

There are two basic ways to start a runbook. The first is by putting the runbook on a schedule. The second is by using a **webhook**.

A [webhook](https://azure.microsoft.com/en-us/documentation/articles/automation-webhooks/) allows you to start a particular runbook in Azure Automation through a single HTTPS request. This allows external services such as Visual Studio Team Services, GitHub, or custom applications to start runbooks without implementing a full solution by using the Azure Automation API.

![]( ../../Linked_Image_Files/1.5.4.png)

Configuring a webhook is simple enough:

<table>
<tbody>
<tr>
<td width="35%">



![]( ../../Linked_Image_Files/1.5.5.png)

</td>
<td>


For security reasons, you can only view the URL in the Azure portal at the time the webhook is created. You should note the URL in a secure location for future use.

**Name**: You can provide any name you want for a webhook because this information is not exposed to the client. It is only used for you to identify the runbook in Azure Automation.

**URL**: The URL of the webhook is the unique address that a client calls with an HTTP POST to start the runbook linked to the webhook. It is automatically generated when you create the webhook. You cannot specify a custom URL. The URL contains a security token that allows the runbook to be invoked by a third-party system with no further authentication. For this reason, it should be treated like a password for security purposes.

**Enabled**: A webhook is enabled by default when it is created.

**Expires**: Like a certificate, each webhook has an expiration date at which time it can no longer be used. This expiration date cannot be changed after the webhook is created, and the webhook also cannot be enabled again after the expiration date is reached. 

A webhook can define values for runbook parameters that are used when the runbook is started by that webhook. The webhook must include values for any mandatory parameters of the runbook and may include values for optional parameters.

</td>
</tr>
</tbody>
</table>

# Azure and Infrastructure as Code  

![Azure cloud image.](../../Linked_Image_Files//0.2.2.png)

Microsoft Azure is built with Infrastructure as Code (IaC) and includes tools that help facilitate the discipline's adoption. Azure Resource Manager has been built from the ground up to support all the IaC principles.

Resource Manager works with resource providers. Each resource provider, such as Azure Compute, Azure Storage, or Azure Network, is responsible for creating the underlying resource, and Resource Manager orchestrates all providers. Every Azure component is exposed via an application program interface (API) that grants you fine control over all parts of your infrastructure. The API can be invoked through the *cross platform* [Azure Command Line Interface](https://azure.microsoft.com/en-us/documentation/articles/xplat-cli-install/) or [Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/powershell-install-configure/), which has also been recently open sourced and now supports cross-platform use. These connections let the creation of infrastructure as a service (IaaS) or platform as a service (PaaS) assets be scripted and run for any platform. A more in-depth discussion of IaaS and PaaS benefits and differences is provided in Module 4 of this course.

![Illustration showing what falls under PaaS and IaaS.](../../Linked_Image_Files//0.2.3.png)

Beyond the creation of Azure assets, tools like [Azure Automation](https://azure.microsoft.com/en-us/services/automation/) and [Desired State Configuration](https://msdn.microsoft.com/en-us/PowerShell/dsc/overview) allow for deeper integration with services once they are deployed to configure the environment. Azure is a first-class platform for Linux and open-source technology, and there is a great story to tell about [support for open source on Azure.](https://azure.microsoft.com/en-us/blog/expanding-linux-and-oss-support-on-azure/) Nearly one in three Azure virtual machines run Linux, and there is an open-source project for [Desired State Configuration for Linux](https://github.com/Microsoft/PowerShell-DSC-for-Linux/releases).

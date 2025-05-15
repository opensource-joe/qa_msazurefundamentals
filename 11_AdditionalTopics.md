# AZ-900 Exam Prep - Additional Topics

- Azure Regions - MS has dozens of Azure regions around the world, grouped into geographies.
- Each geography meets data residency and compliance requirements.
- Paired Regions - UK geography contains two regions: UK South and UK West. If there is an Azure outage that affects multiple regions, then at least one region in each regional pair will be prioritized for recovery.

- Resource Group - used to organize a set of related resources. 
- Details about Resource Groups:
    - Can't put a resource in more than one resource group.
    - Can move a resource from one resource group to another.
    - Can move a resource from one subscription to another.
    - Resources don't need to be in the same region as the resource group they are in.
    - Tags are simply labels that can apply to resources for management purposes - can do by department for charging appropriately.
    - Tags applied to a resource group don't get inherited by its resources.
    - When a resource group is deleted, all the of resources get deleted too.

- Azure provides three types of logs for troubleshooting and reporting.
    - Resource logs - contain info about things that happened within an Azure resource.
    - Activity logs - contain info at the subscription level about activities that were performed on a resource from the outside.
    - Azure Active Directory logs - contain info about activities specifically related to Azure Active Directory.
    - Note: MS Entra logs contain information about activities specifically related to Microsoft Entra ID, such as recent logins and new users added.

- Locks
    - Delete - prevents resource from being deleted.
    - Read-Only - prevents a resource from being deleted or modified.
    - Latest lock applied by Administrator is added. If want to delete resource, then need to delete the lock.
    - To lock all of the resources in a resource group, you only have to apply the lock to the resource group itself. Can also do at subscription level.

- Azure Policy - lets you enforce a wide variety of governance policies. Can assign to the Resource Group. Can group similar policies for multiple Resource Groups, Subscriptions, and Management Groups through an Initiative.

- Management Groups - when organization has a lot of subscriptions, you'll want to apply the same policies or policy initiatives to many of them.
- Can put subscriptions in management groups and apply a policy or role assignment to a management group.

- Trust Center - contains a collection of links to resources about how Microsoft handles security, privacy, compliance, and transparency.
- Service Trust Portal - focused specifically on compliance. For example, it has links to Azure audit reports for regulatory standards like SOC, FedRAMP, and ISO27001.
- Compliance Manager - shows how compliant MS and your organization is with various policies (GDPR, NIST). Helps with maintaining cloud compliance.

- Azure Government Services - located in physically isolated data centers and networks. Available to US government at the federal, state, and local levels, as well as to their partners. Org has to meet eligibility requirements.

- China region - managed by 21Vianet.

- Azure Virtual Desktop - another type of VM. desktop and application virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location. Azure Virtual Desktop works across devices and operating systems, and works with apps that you can use to access remote desktops or most modern browsers.

- MS Purview Data Governance - manage, understand, and govern your data with confidence. Maximize the value of your data estate with an AI-powered, business- friendly, and unified approach.

- Azure Arc - simplifies governance and management by delivering a consistent multicloud and on-premises management platform.

- IaC - Infrastructure as code (IaC) uses DevOps methodology and versioning with a descriptive model to define and deploy infrastructure, such as networks, virtual machines, load balancers, and connection topologies. Just as the same source code always generates the same binary, an IaC model generates the same environment every time it deploys. IaC is a key DevOps practice and a component of continuous delivery. With IaC, DevOps teams can work together with a unified set of practices and tools to deliver applications and their supporting infrastructure rapidly and reliably at scale.

- IaaS - Infrastructure-as-a-Service includes compute, storage, and networking services. Some examples are Azure Virtual Machines, Azure Storage, and Azure Virtual Networks. Platform-as-a-Services refers to services that manage the underlying infrastructure for you. Some examples are Azure App Service, Azure SQL Database, and Azure Cosmos DB.
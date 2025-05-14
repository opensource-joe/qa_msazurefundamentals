# Overview of Azure Services

- Collection of online services accessed over the Internet. Don't need physical resources, pay for what you use, and scale as needed.
- Need compute, storage, and networking.

- Compute:
    1) Azure Virtual Machines (IaaS)
    2) Azure App Service (PaaS) - only for web and mobile apps
    3) Azure Container Instances
    4) Azure Kubernetes Services - used for orchestration for multi-container services
    5) Azure Functions - serverless offering, use and pay for only when function is running

- Storage:
    1) Azure Blob Storage - object storage, unstructured data, flat file; hot, cool, and archive storage
    2) Azure File Storage - traditional hierarchical DB
    3) Azure Data Lake Storage
    4) Azure SQL Database
    5) Azure DB for Open Source - MySQL, Hadoop
    6) Azure Synapse Analytics - data warehouse
    7) Azure Cosmos DB - no SQL offering
    8) Azure Cache for Redis - no SQL, speed up applications with caching

- Network
    1) VNet
    2) Subnets
    3) VNet Peering
    4) Azure VPN - encrypted routing
    5) Azure ExpressRoute - private dedication connection

- Other services - AI, DevOps

- Using the Azure Portal
    - Use the web interface, powershell, CLI, or SDK
    - Can use powershell and CLI in the browser
    - Also a mobile app

- Azure account
    - Billing and subscription accounts
    - Multiple subscriptions under a billing account
    - Resource groups and their resources can be divided into subscriptions

- Regions with availability zones will have three data centers; choose the region closest to customers.

- Designing a solution - can use standard templates for solutions.

- Managing services aka Management
    1) Azure Monitor
    2) Azure Backup - can backup cloud and on-prem solutions
    3) Azure Advisor - provides security recommendations; suggest ways to improve the performance and availability of your applications, but it will even suggest ways to reduce your costs;  personalized cloud consultant. It automatically examines all of your Azure resources and identifies ways to optimize them.
    4) MS Defender for Cloud - assesses vulnerabilities
    5) Azure Policy - create own custom policy for resources
    6) Advanced Threat Detection
    7) ARM Template - automate resource deployment
    8) Azure Blueprints - automate env deployment

- Azure IoT Central is a fully managed SaaS solution that allows you to create IoT applications without writing any code.

- Azure Sphere to make your IoT devices more secure. It includes certified chips, the Azure Sphere operating system, and the Azure Sphere Security Service, all of which provide layers of protection for your IoT devices.
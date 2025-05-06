# Intro to Azure App Service

- Used for deploying web apps through a PaaS b/c it manages the underlying infrastructure. 
- Supports a wide variety of languages and frameworks - ASP.Net, Java, Ruby, Node.JS, PHP, Python.
- Can choose to run on Windows or Linux.
- Can use different program language by using a Docker container.
- Integrations include VSCode, Azure DevOps, GitHub, and BitBucket. 
- Can also use for mobile backends and APIs.
- Had enterprise class features - high availability (99.95% uptime), scalability to automatically add resources when demand increases, security with authentication and IP address access control.

- App Service Plans
    - Operating System - Windows or Linux
    - Region - choose one closest to users. Can't change it later, would need to make a copy for new service plan.
    - Pricing Tier - table to choose compute, network, etc.
    * Can put multiple apps in one service plan. Too many apps could cause performance issues. Could scale out by adding more VMs or setup auto-scaling. Another option is to scale up by using a bigger pricing tier w/ more compute.
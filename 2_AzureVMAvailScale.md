# Azure Virtual Machine Availability and Scalability Solutions

- VMs give full control over software and operating system. Especially useful for migrating services to the cloud.

- High availability - application will continue to run even if there's a hardware failure or otherwise adverse event.
    - Availability set - not recommended anymore. A group of VMs that can handle planned and unplanned downtime.
    - Planned downtime - Azure updates infrastructure and reboots VMs.
    - Unplanned downtime - VM goes down unexpectedly. 

- Planned downtime - VMs grouped into update domains. Azure performs maintenance on one update domain at a time. Configure up to 20 domains.
- Unplanned downtimes - VMs grouped in fault domains. Each default domain has a separate power source and network switch. Limits downtime caused by hardware failures. In many regions, maximum of three fault domains, but in some it's two.

- For 99.95% uptime guarantee, need at least two VMs, two default domains, and two update domains. Won't protect against datacenter failures.
- Availability zones are alternative to availability sets. Physically separate zones within an Azure region. Three zones per region. Won't protect against regional outlets. 
- Multi-region deployment - usually sufficient to back up VMs to second region. If downtime can't be tolerated, run VMs in second region all the time.
- Regional pairs - most Azure regions are paired with another region. Some services replicate their data across regional pairs if certain options are chosen (e.g., Azure Storage with geo-redundant storage option). Store VMs in paired region. MS tries to make at least one region in each pair available.

- Scalability - ability to handle spikes in demand.
    - Vertical scaling - switch VM to larger size. Easy to do but has limitations.
    - Horizontal scaling - adding more VMs. More complicated. Make application stateless to run across multiple machines (the VM should not store any data locally).
    - Scale Sets - VMs are distributed across fault domains and update domains. Automatically increase or decrease the number of VMs according to rules you define. Can use disk and network metrics. To use guest operating system metrics, enable diagnostics extension. Can set limits on min/max number of VMs. Can have up to 1,000 VMs in a Scale Set (600 with custom VM images). Setting a max is a good idea.

        - Zonal Scale Set - default for Scale Set deployed in a single zone.
        - Regional Scale Set - ultimate deployment with max availability. VMs evenly distributed across availability zones.
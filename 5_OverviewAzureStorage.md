# Overview of Azure Storage

- Azure DB - need to store data on Azure but don't need a full DB.
    1) Durable and highly available: stores all data redundantly.
    2) Secure: all data is encrypted automatically, and you can set fine grained access control.
    3) Scalable: add more data without provisioning hardware with 5-petabyte limit and can get more if needed.
    4) Managed service: maintenance not necessary.
    5) Accessible over the web.

    - Supports four types of data - blobs, files, queues, and tables.
    - Storage Account - section for each type of data. Blobs containers b/c they need a container first.
    
    - Binary Large Object - BLOB. Not organized. Can make hierarchical w/ Azure Data Lake Storage Gen2.
        - Choose from three access tiers.
            - Hot - frequently accessed data.
            - Cool - infrequently accessed data. Lower storage cost but higher cost for reads and writes. Data must be in cool tier for at least 30 days.
            - Archive - rarely accessed data. May take up to 15 hours to access data. 5x cheaper than cool tier for storage but much more expensive for reads. Data must be in archive tier for at least 180 days.
            * Can move data between tiers anytime but will be charged if moving data before minimum time then will be assessed a deletion fee.
            * Can set every BLOB by tier. Can have lifecycle management rules too.
    
    - File Storage - SMB compliant and hierarchical. Can be globally accessible over the web w/ a token. More expensive than BLOB storage.

    - Queue Storage - intended for passing messages between applications. One application pushes messages onto the queue and another application asynchronously retrieves the messages and processes them.

    - Table Storage - nosql datastore with storage costs equivalent to file storage. Transaction costs significantly cheaper than file store. Premium version available as part of the Cosmos DB service.

    - Disk Storage - used for disks attached to the VMs. Created w/ a VM, don't need to create in Azure storage.

    - Geo-Redundant Options (least to most redundant)
        1) Locally Redundant Storage (LRS) - replicated across racks in the same data center. Only use LRS if you can reconstruct your data.
        2) Zone Redundant Storage (ZRS) - replicated across three zones in one region. If one zone goes down, data still available in another region.
        3) Geo-Redundant Storage (GRS) - replicated across two regions. If region goes down, data available in another region. In the event of a regional disaster, you must perform a geo-failover to access data in the secondary region.
        4) Read-Access Geo-Redundant Storage (RAGRS) - same as Geo-Redundant with regional disaster, data can be read from secondary region immediately. Write access is unavailable until MS restores availability in the primary region. If write access is required sooner, you must copy your data to another region.
        5) Geo-Zone Redundant Storage (GZRS) - almost same as GRS with a critical difference. Combination of zone redundant storage and geo-redundant storage.
        6) Read-Access Geo-Zone-Redundant Storage (RA-GZRS) - RA-GZRS is same as RA-GRS except that data is copied to three availability zones in the primary region.
        * For all geo-redundant options, if the primary region fails, the data in the secondary region will likely be slightly out of date. 

- Copy files to storage using CLI and AzCopy. Let's you copy files and folders to or from a storage account and between Azure and other cloud providers. Can also use Azure Storage Explorer through Azure Portal.

- Azure File Sync - create local cache of files and sync with agent on Windows server. This lets user access file share more quickly with specialized use case.

- Migrating on-prem to Azure.
    1) Azure Migrate - discovers on-prem servers, web apps, and databases. Assess them and tells you the size and cost of the equivalent Azure services. Helps you do the migration.
    2) Azure Data Box - for large amounts of data during migration. MS ships Data Box storage device to data center. Copy data to device and ship back to MS. MS transfers the data from the device to your Azure storage account. Can also use Data Box to export data from Azure to your data center. Only use if need to transfer 40 terabytes of data or more.
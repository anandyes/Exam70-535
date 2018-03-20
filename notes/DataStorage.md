## Design Data Implementation (15 - 20 %)

### Determine when to use Azure Blob Storage, blob tiers, Azure Files, disks, and StorSimple

* Blob Storage
  * Types - Block Blobs, Page Blobs, Append Blobs
  * Supports streaming and random access scenarios
  * REST APIs
  * LRS, ZRS, GRS, RA-GRS
  * Capacity - up to 500 TB containers
  * Object Size - Up to 200 GB/block blob
  
* Azure Files
  * Network file share using SMB
  * REST APIs, SMB 2.1 (Within region) and SMB 3.0 (Worldwide)
  * AD ACLs are not supported
  * Lift and Shift applications to cloud
  * LRS, ZRS, GRS
  * Capacity - up to 1TB/file 
  * Object Size - Up to 1TB/file
  * Shared accross multiple VMs
  * 1000 IOps
  * Max Size - 5 TB File Share and 1 TB file within share

* Disk Storage
  * provides managed and unmanage disk capabilities
  * persistant data accessible from within the VM (VHDs)
  * Scope - single VM
  * Provides Snapshots and Copy
  * Built-in authentication
  * Files within VHD cannot be accessed
  * 500 IOps
  * Max Size - 4 TB disk
  
* Queue Storage
  * Messages can be up to 64 KB in size
* Table Storage
  * stores structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design

### Types of Storage accounts

* General Purpose Storage accounts - 
  * Standard - uses Magnetic media to store data
  * Premium - uses SSD to store data
* Blob Storage accounts
  * Stores Block blobs and Append blobs. Page blobs cannot be stored
  * Access tiers - Hot or Cool
  * Hot for frequent data access Higher cost for storage but cost of access is low
  * Cool access tier - Cost of storage is less and higher cost for accessing blobs

### Securing access to Storage
* controlling access to storage account key using RBAC in Azure AD
* using shared access signatures.
* pulic access to blobs for anonymous read
  
#### SAS (Shared Access Signature)[^](https://docs.microsoft.com/en-us/azure/storage/common/storage-dotnet-shared-access-signature-part-1)
* Provides access to Storage account resources to clients without sharing storage account keys
* Types of Access Control
  * Time Interval
  * Permissions (read, write , delete)
  * IP address
  * Protocol
* When to used SAS?
  * When Clients upload data via a front-end proxy
  * Access Storage directly with permissions defined by SAS
  * When copying Blobs to Blobs, Files to Files and Blobs to Files
* Types of SAS
  * Service SAS
  * Account SAS
* SAS is a signed URI that has Resource URI and SAS token

### Encryption

* Encryption at rest - Azure Storage Service Encryption (SSE) at rest
  * automatically encrypts data prior to persisting to storage and decrypts prior to retrieval.
  * Standard and Premium tiers
* Client-side encryption
  * Storage client libraries
  
### Replication
* Locally-redundant storage (LRS)
  *  99.999999999% (11 9's) durability
* Zone-redundant storage (ZRS) (Preview)
  * at least 99.9999999999% (12 9's) durability
  * synchronous data replication across multiple availability zones
  * ZRS Classic available for block blobs in gen purpose v1 account for asynchronous replication across one or two regions.
  
* Geo-redundant storage (GRS)
  * provide 99.99999999999999% (16 9's) durability
  * local copies of data in primary region and copies in secondary region
  
* Read-access geo-redundant storage (RA-GRS)
  * provides read access to data in secondary region

### Transfering Data to and from storage
* AZCopy tool for Windows and Linux
* Azure Import/Export services - for large amounts of blob data using hard drives

### StorSimple
* Microsoft Azure StorSimple device -  an on-premises hybrid storage array that contains SSDs and HDDs, together with redundant controllers and automatic failover capabilities.
* StorSimple Cloud Appliance (Virtual Appliance) - is a software version of the StorSimple device that replicates the architecture and most capabilities of the physical hybrid storage device
* The Microsoft Azure StorSimple Virtual Array is an integrated storage solution that manages storage tasks between an on-premises virtual array running in a hypervisor and Microsoft Azure cloud storage.
* The virtual array is particularly well-suited for the storage of infrequently accessed archival data.
* The virtual array has a maximum capacity of 6.4 TB on the device (with an underlying storage requirement of 8 TB) and 64 TB including cloud storage.

### Storage Analytics
* Azure Storage Analytics performs logging and provides metrics data for a storage account
* Storage Analytics metrics are available for the Blob, Queue, Table, and File services
* Storage Analytics logging is available for the Blob, Queue, and Table services
* Storage account with ZRS do not have metrics and logging capabilities
* Storage Analytics has a 20TB limit independent of storage account limit

### CORS (Cross-Origin Resource Sharing) Support for Azure Services
* CORS is an HTTP feature that enables a web application running under one domain to access resources in another domain.
* Web browsers implement a security restriction known as same-origin policy that prevents a web page from calling APIs in a different domain
* CORS provides a secure way to allow one domain (the origin domain) to call APIs in another domain.
* CORS is not supported for Premium Storage accounts
* CORS to be enabled for each service (Blob, File, Queue and Table) separately
* By default, CORS is disabled for each service

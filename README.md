<aside class="notice">
**********************************Disclaimer**********************************

###### This guide is being updated as I am preparing for the Exam 70-535. All the content refered here are in public domain and not my creation. This this just a collection for easy reference. Use with your own discretion.

******************************************************************************
</aside>

# Architecting Microsoft Azure Solutions (70-535)
## 1. Design Compute Infrastructure (20-25%)
### 1.1 Design solutions using virtual machines 
* Design VM deployments by leveraging availability sets, fault domains, and update domains in Azure; use web app for containers; design VM Scale Sets; design for compute-intensive tasks using Azure Batch; define a migration strategy from cloud services; recommend use of Azure Backup and Azure Site Recovery

#### Links:

1. [Create a Windows virtual machine with the Azure portal](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal) 
2. [How to use availability sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-availability-sets) ,
[Manage Availability sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/manage-availability) 
3. [Azure Exam Prep – Fault Domains and Update Domains](https://blogs.msdn.microsoft.com/plankytronixx/2015/05/01/azure-exam-prep-fault-domains-and-update-domains/) 
4. [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/manage-availability/) 
5. [Use a custom Docker image for Web App for Containers](https://docs.microsoft.com/en-us/azure/app-service/containers/tutorial-custom-docker-image) 
6. [What are virtual machine scale sets in Azure?](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-overview)
7. [Run intrinsically parallel workloads with Batch](https://docs.microsoft.com/en-us/azure/batch/batch-technical-overview) 
8. [About Azure Migrate](https://docs.microsoft.com/en-us/azure/migrate/migrate-overview) 
9. [Back up Azure virtual machines to a Recovery Services vault](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-vms)
10. [About Site Recovery](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-overview) 

#### Recommended high availability "best practices" for virtual machines deployment:
- Configure multiple virtual machines in an availability set - for redundancy
- Use managed disks for VMs in an availability set
- Use Scheduled Events to proactively response to VM impacting events
- Configure each application tier into separate availability sets
- Combine a Load Balancer with availability sets
- Use availability zones to protect from datacenter level failures

### 1.2 Design solutions for serverless computing 
* Use Azure Functions to implement event-driven actions; design for serverless computing using Azure Container Instances; design application solutions by using Azure Logic Apps, Azure Functions, or both; determine when to use API management service
### 1.3 Design microservices-based solutions   
* Determine when a container-based solution is appropriate; determine when container-orchestration is appropriate; determine when Azure Service Fabric (ASF) is appropriate; determine when Azure Functions is appropriate; determine when to use API management service; determine when Web API is appropriate; determine which platform is appropriate for container orchestration; consider migrating existing assets versus cloud native deployment; design lifecycle management strategies
### 1.4 Design web applications 
* Design Azure App Service Web Apps; design custom web API; secure Web API; design Web Apps for scalability and performance; design for high availability using Azure Web Apps in multiple regions; determine which App service plan to use; design Web Apps for business continuity; determine when to use Azure App Service Environment (ASE); design for API apps; determine when to use API management service; determine when to use Web Apps on Linux; determine when to use a CDN; determine when to use a cache, including Azure Redis cache
### 1.5 Create compute-intensive application 
* Design high-performance computing (HPC) and other compute-intensive applications using Azure Services; determine when to use Azure Batch; design stateless components to accommodate scale; design lifecycle strategy for Azure Batch

## 2. Design Data Implementation (15-20%)
### 2.1 Design for Azure Storage solutions
Determine when to use Azure Blob Storage, blob tiers, Azure Files, disks, and StorSimple
### 2.2 Design for Azure Data Services
Determine when to use Data Catalog, Azure Data Factory, SQL Data Warehouse, Azure Data Lake Analytics, Azure Analysis Services, and Azure HDInsight
### 2.3 Design for relational database storage
Determine when to use Azure SQL Database and SQL Server Stretch Database; design for scalability and features; determine when to use Azure Database for MySQL and Azure Database for PostgreSQL; design for HA/DR, geo-replication; design a backup and recovery strategy

* [SQL Database Automated Backups](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-automated-backups)
* [Long-term backup retension upto 10 years using Azure Recovery Services vault](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-long-term-retention)
* [Business continuity overview](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-business-continuity)
* [Designing highly available services using Azure SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-designing-cloud-solutions-for-disaster-recovery)
* [Disaster recovery strategies for applications using SQL Database elastic pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-disaster-recovery-strategies-for-applications-with-elastic-pool)

### 2.4 Design for NoSQL storage
Determine when to use Azure Redis Cache, Azure Table Storage, Azure Data Lake, Azure Search, Time Series Insights
### 2.5 Design for CosmosDB storage
Determine when to use MongoDB API, DocumentDB API, Graph API, Azure Tables API; design for cost, performance, data consistency, availability, and business continuity

## 3. Design Networking Implementation (15-20%)
### 3.1 Design Azure virtual networks
Design solutions that use Azure networking services: design for load balancing using Azure Load Balancer and Azure Traffic Manager; define DNS, DHCP, and IP strategies; determine when to use Azure Application Gateway; determine when to use multi-node application gateways, Traffic Manager and load balancers
### 3.2 Design external connectivity for Azure Virtual Networks
Determine when to use Azure VPN, ExpressRoute and Virtual Network Peering architecture and design; determine when to use User Defined Routes (UDRs); determine when to use VPN gateway site-to-site failover for ExpressRoute
### 3.3 Design security strategies
Determine when to use network virtual appliances; design a perimeter network (DMZ); determine when to use a Web Application Firewall (WAF), Network Security Group (NSG), and virtual network service tunneling
### 3.4 Design connectivity for hybrid applications
Design connectivity to on-premises data from Azure applications using Azure Relay Service, Azure Data Management Gateway for Data Factory, Azure On-Premises Data Gateway, Hybrid Connections, or Azure Web App’s virtual private network (VPN) capability; identify constraints for connectivity with VPN; identify options for joining VMs to domains

## 4. Design Security and Identity Solutions (20-25%)
### 4.1 Design an identity solution
Design AD Connect synchronization; design federated identities using Active Directory Federation Services (AD FS); design solutions for Multi-Factor Authentication (MFA); design an architecture using Active Directory on-premises and Azure Active Directory (AAD); determine when to use Azure AD Domain Services; design security for Mobile Apps using AAD
### 4.2 Secure resources by using identity providers
Design solutions that use external or consumer identity providers such as Microsoft account, Facebook, Google, and Yahoo; determine when to use Azure AD B2C and Azure AD B2B; design mobile apps using AAD B2C or AAD B2B
### 4.3 Design a data security solution
Design data security solutions for Azure services; determine when to use Azure Storage encryption, Azure Disk Encryption, Azure SQL Database security capabilities, and Azure Key Vault; design for protecting secrets in ARM templates using Azure Key Vault; design for protecting application secrets
using Azure Key Vault; design a solution for managing certificates using Azure Key Vault; design solutions that use Azure AD Managed Service Identity
### 4.4 Design a mechanism of governance and policies for administering Azure resources
Determine when to use Azure RBAC standard roles and custom roles; define an Azure RBAC strategy; determine when to use Azure resource policies; determine when to use Azure AD Privileged Identity Management; design solutions that use Azure AD Managed Service Identity; determine when to use HSM-backed keys
### 4.5 Manage security risks by using an appropriate security solution
Identify, assess, and mitigate security risks by using Azure Security Center, Operations Management Suite Security and Audit solutions, and other services; determine when to use Azure AD Identity Protection; determine when to use Advanced Threat Detection; determine an appropriate endpoint protection strategy

## 5. Design Solutions by using Platform Services (10-15%)
### 5.1 Design for Artificial Intelligence Services
Determine when to use the appropriate Cognitive Services, Azure Bot Service, Azure Machine Learning, and other categories that fall under cognitive AI
### 5.2 Design for IoT
Determine when to use Stream Analytics, IoT Hubs, Event Hubs, real-time analytics, Time Series Insights, IoT Edge, Notification Hubs, Event Grid, and other categories that fall under IoT
### 5.3 Design messaging solution architectures
Design a messaging architecture; determine when to use Azure Storage Queues, Azure Service Bus, Azure Event Hubs, Event Grid, Azure Relay, Azure Functions, and Azure Logic Apps; design a push notification strategy for Mobile Apps; design for performance and scale
### 5.4 Design for media service solutions
Define solutions using Azure Media Services, video indexer, video API, computer vision API, preview, and other media related services

## 6. Design for Operations (10-15%)
### 6.1 Design an application monitoring and alerting strategy
Determine the appropriate Microsoft products and services for monitoring applications on Azure; define solutions for analyzing logs and enabling alerts using Azure Log Analytics; define solutions for analyzing performance metrics and enabling alerts using Azure Monitor; define a solution for monitoring applications and enabling alerts using Application Insights
### 6.2 Design a platform monitoring and alerting strategy
Determine the appropriate Microsoft products and services for monitoring Azure platform solutions; define a monitoring solution using Azure Health, Azure Advisor, and Activity Log; define a monitoring solution for Azure Networks using Log Analytics and Network Watcher service; monitor security with Azure Security Center
### 6.3 Design an operations automation strategy
Determine when to use Azure Automation, Chef, Puppet, PowerShell, Desired State Configuration (DSC), Event Grid, and Azure Logic Apps; define a strategy for auto-scaling; define a strategy for enabling periodic processes and tasks
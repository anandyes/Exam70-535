||
|:-:|
| Disclaimer: This guide is being updated as I am preparing for the Exam 70-535. All the content referred here are available in public domain and not my creation. This is just a collection for easy reference. Use it with your own discretion. |
||

# Architecting Microsoft Azure Solutions (70-535)[^](https://www.microsoft.com/en-us/learning/exam-70-535.aspx)
## 1. Design Compute Infrastructure (20-25%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=Compute)
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
### 1.3 Design microservices-based solutions [^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=containers)   
* Determine when a container-based solution is appropriate; determine when container-orchestration is appropriate; determine when Azure Service Fabric (ASF) is appropriate; determine when Azure Functions is appropriate; determine when to use API management service; determine when Web API is appropriate; determine which platform is appropriate for container orchestration; consider migrating existing assets versus cloud native deployment; design lifecycle management strategies
### 1.4 Design web applications [^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=web)
* Design Azure App Service Web Apps; design custom web API; secure Web API; design Web Apps for scalability and performance; design for high availability using Azure Web Apps in multiple regions; determine which App service plan to use; design Web Apps for business continuity; determine when to use Azure App Service Environment (ASE); design for API apps; determine when to use API management service; determine when to use Web Apps on Linux; determine when to use a CDN; determine when to use a cache, including Azure Redis cache
### 1.5 Create compute-intensive application 
* Design high-performance computing (HPC) and other compute-intensive applications using Azure Services; determine when to use Azure Batch; design stateless components to accommodate scale; design lifecycle strategy for Azure Batch

## 2. Design Data Implementation (15-20%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=storage)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=databases)
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

## 3. Design Networking Implementation (15-20%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=network)
### 3.1 Design Azure virtual networks
Design solutions that use Azure networking services: design for load balancing using Azure Load Balancer and Azure Traffic Manager; define DNS, DHCP, and IP strategies; determine when to use Azure Application Gateway; determine when to use multi-node application gateways, Traffic Manager and load balancers
### 3.2 Design external connectivity for Azure Virtual Networks
Determine when to use Azure VPN, ExpressRoute and Virtual Network Peering architecture and design; determine when to use User Defined Routes (UDRs); determine when to use VPN gateway site-to-site failover for ExpressRoute
### 3.3 Design security strategies
Determine when to use network virtual appliances; design a perimeter network (DMZ); determine when to use a Web Application Firewall (WAF), Network Security Group (NSG), and virtual network service tunneling
### 3.4 Design connectivity for hybrid applications
Design connectivity to on-premises data from Azure applications using Azure Relay Service[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-hybrid-connections), Azure Data Management Gateway for Data Factory, Azure On-Premises Data Gateway, Hybrid Connections, or Azure Web App’s virtual private network (VPN) capability; identify constraints for connectivity with VPN; identify options for joining VMs to domains

## 4. Design Security and Identity Solutions (20-25%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=security)
### 4.1 Design an identity solution
* Design AD Connect synchronization[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect); 
* Design federated identities using Active Directory Federation Services (AD FS)[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-azure-adfs);
* Design solutions for Multi-Factor Authentication (MFA)[^](https://docs.microsoft.com/en-us/azure/multi-factor-authentication/); 
* Design an architecture using Active Directory on-premises and Azure Active Directory (AAD)[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect); 
* Determine when to use Azure AD Domain Services[^](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-overview); 
* Design security for Mobile Apps using AAD[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-authentication-overview)[^](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-scenarios)

Notes:
* [Azure AD Notes](notes/AzureAD.md)
* [Introduction to Azure Security](https://docs.microsoft.com/en-us/azure/security/azure-security)

### 4.2 Secure resources by using identity providers
* Design solutions that use external or consumer identity providers such as Microsoft account, Facebook, Google, and Yahoo;[^](https://docs.microsoft.com/en-us/azure/active-directory-b2c/active-directory-b2c-overview) 
* Determine when to use Azure AD B2C and Azure AD B2B[^](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-compare-b2c); 
*  Design mobile apps using AAD B2C or AAD B2B [^](https://docs.microsoft.com/en-us/azure/active-directory-b2c/active-directory-b2c-reference-oauth-code)
### 4.3 Design a data security solution
* Design data security solutions for Azure services[^](https://docs.microsoft.com/en-us/azure/security/security-azure-encryption-overview); 
* Determine when to use Azure Storage encryption[^](https://docs.microsoft.com/en-us/azure/storage/common/storage-service-encryption), Azure Disk Encryption[^](https://docs.microsoft.com/en-us/azure/security/azure-security-disk-encryption), Azure SQL Database security capabilities[^](https://docs.microsoft.com/en-us/azure/security/azure-database-security-overview), and Azure Key Vault[^](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-whatis); 
* Design for protecting secrets in ARM templates using Azure Key Vault[^](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-keyvault-parameter); 
* Design for protecting application secrets using Azure Key Vault[^](https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/key-vault);
* Design a solution for managing certificates using Azure Key Vault[^](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)[^](http://www.rahulpnath.com/blog/manage-certificates-in-azure-key-vault/); 
* Design solutions that use Azure AD Managed Service Identity[^](https://docs.microsoft.com/en-us/azure/active-directory/managed-service-identity/overview)

Note: The Azure SQL Database service is only available through TCP port 1433.

Useful Links :
* [Azure Database Security Best Practices](https://docs.microsoft.com/azure/security/azure-database-security-best-practices)

### 4.4 Design a mechanism of governance and policies for administering Azure resources
* Determine when to use Azure RBAC standard roles and custom roles[^](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-what-is); 
* Define an Azure RBAC strategy[^](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-configure);
* Determine when to use Azure resource policies[^](https://docs.microsoft.com/en-us/azure/azure-policy/azure-policy-introduction); 
* Determine when to use Azure AD Privileged Identity Management[^](https://docs.microsoft.com/en-us/azure/active-directory/privileged-identity-management/azure-pim-resource-rbac); 
* Design solutions that use Azure AD Managed Service Identity[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-managed-service-identity); 
* Determine when to use HSM-backed keys[^](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-hsm-protected-keys)[^](https://blogs.technet.microsoft.com/kv/2015/01/08/azure-key-vault-making-the-cloud-safer/)
### 4.5 Manage security risks by using an appropriate security solution
* Identify, assess, and mitigate security risks by using Azure Security Center[^](https://docs.microsoft.com/en-us/azure/security-center/security-center-get-started), Operations Management Suite Security and Audit solutions, and other services[^](https://docs.microsoft.com/en-us/azure/operations-management-suite/oms-security-getting-started); 
* Determine when to use Azure AD Identity Protection[^](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-identityprotection); 
* Determine when to use Advanced Threat Detection[^](https://docs.microsoft.com/en-us/azure/security/azure-threat-detection); 
* Determine an appropriate endpoint protection strategy[^](https://docs.microsoft.com/en-us/azure/security/azure-security-antimalware)[^](https://docs.microsoft.com/en-us/azure/security-center/security-center-install-endpoint-protection)

## 5. Design Solutions by using Platform Services (10-15%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=ai)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=iot)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=integration)
### 5.1 Design for Artificial Intelligence Services
Determine when to use the appropriate Cognitive Services, Azure Bot Service, Azure Machine Learning, and other categories that fall under cognitive AI
### 5.2 Design for IoT
Determine when to use Stream Analytics, IoT Hubs, Event Hubs, real-time analytics, Time Series Insights, IoT Edge, Notification Hubs, Event Grid, and other categories that fall under IoT
### 5.3 Design messaging solution architectures
Design a messaging architecture; determine when to use Azure Storage Queues, Azure Service Bus, Azure Event Hubs, Event Grid, Azure Relay, Azure Functions, and Azure Logic Apps; design a push notification strategy for Mobile Apps; design for performance and scale
### 5.4 Design for media service solutions
Define solutions using Azure Media Services, video indexer, video API, computer vision API, preview, and other media related services

## 6. Design for Operations (10-15%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=mgmt)
### 6.1 Design an application monitoring and alerting strategy
* Determine the appropriate Microsoft products and services for monitoring applications on Azure; 
* Define solutions for analyzing logs and enabling alerts using Azure Log Analytics[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-overview);
* Define solutions for analyzing performance metrics and enabling alerts using Azure Monitor; 
* Define a solution for monitoring applications and enabling alerts using Application Insights
### 6.2 Design a platform monitoring and alerting strategy
Determine the appropriate Microsoft products and services for monitoring Azure platform solutions; define a monitoring solution using Azure Health, Azure Advisor, and Activity Log; define a monitoring solution for Azure Networks using Log Analytics and Network Watcher service; monitor security with Azure Security Center
### 6.3 Design an operations automation strategy
Determine when to use Azure Automation, Chef, Puppet, PowerShell, Desired State Configuration (DSC), Event Grid, and Azure Logic Apps; define a strategy for auto-scaling; define a strategy for enabling periodic processes and tasks

## Useful links

* [Avail free training](https://azure.microsoft.com/en-us/training/learning-paths/azure-solution-architect/)
* [Books to study](https://buildazure.com/2018/02/01/book-exam-ref-70-535-architecting-microsoft-azure-solutions/)[^](http://amzn.to/2Fsg5IG)
| Disclaimer: This guide is being updated as I am preparing for the Exam 70-535. All the content referred here are available in public domain and not my creation. This is just a collection for easy reference. Use it with your own discretion. |
|:-:|

# Architecting Microsoft Azure Solutions (70-535)[^](https://www.microsoft.com/en-us/learning/exam-70-535.aspx)
## 1. Design Compute Infrastructure (20-25%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=Compute)
### 1.1 Design solutions using virtual machines[^](notes/Compute.md#virtual-machines) 
* Design VM deployments by leveraging availability sets, fault domains, and update domains in Azure[^](notes/Compute.md#Compute.md#availability-sets-fault-domains-and-update-domains)
* Use web app for containers[^](notes/Compute.md#web-app-for-containers)
* Design VM Scale Sets[^](notes/Compute.md#vm-scale-sets)
* Design for compute-intensive tasks using Azure Batch[^](notes/Compute.md#compute-intensive-tasks-using-azure-batch)
* Define a migration strategy from cloud services[^](notes/Compute.md##migration-strategy-from-cloud-services)
* Recommend use of Azure Backup and Azure Site Recovery[^](notes/Compute.md#azure-backup)
 
### 1.2 Design solutions for serverless computing[^](https://azure.microsoft.com/en-in/overview/serverless-computing/) 
* Use Azure Functions to implement event-driven actions[^](notes/Compute.md#use-azure-functions-)
* Design for serverless computing using Azure Container Instances[^](notes/Compute.md#azure-container-instances)
* Design application solutions by using Azure Logic Apps, Azure Functions, or both[^](notes/Compute.md#design-application-solutions-by-using-azure-logic-apps-)[^](https://docs.microsoft.com/en-in/azure/azure-functions/functions-create-serverless-api)[^](https://docs.microsoft.com/en-in/azure/azure-functions/functions-compare-logic-apps-ms-flow-webjobs)
* Determine when to use API management service[^](notes/Compute.md#api-management-service)

### 1.3 Design microservices-based solutions[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=containers)[^](notes/Compute.md#microservices)   
* Determine when a container-based solution is appropriate[^](notes/Compute.md#azure-container-instances)
* Determine when container-orchestration is appropriate[^](notes/Compute.md#container-orchestration)
* Determine when Azure Service Fabric (ASF) is appropriate[^](notes/Compute.md#azure-service-fabric-asf)
* Determine when Azure Functions is appropriate[^](https://docs.microsoft.com/en-in/azure/azure-functions/functions-overview)
* Determine when to use API management service[^](notes/Compute.md#api-management-service)
* Determine when Web API is appropriate[^](notes/Compute.md#custom-web-api)
* Determine which platform is appropriate for container orchestration[^](notes/Compute.md#container-orchestration)
* Consider migrating existing assets versus cloud native deployment[^](https://docs.microsoft.com/en-us/dotnet/standard/modernize-with-azure-and-containers/)
* Design lifecycle management strategies

### 1.4 Design web applications [^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=web)[^](notes/Compute.md#web-applications)
* Design Azure App Service Web Apps[^](https://docs.microsoft.com/en-us/azure/app-service/)[^](notes/Compute.md#azure-app-service-)
* Design custom web API [^](notes/Compute.md#custom-web-api)
* Secure Web API[^](notes/Compute.md#secure-web-api)
* Design Web Apps for scalability and performance[^](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/scalable-web-app)
* Design for high availability using Azure Web Apps in multiple regions[^](notes/Compute.md#multi-region-)
* Determine which App service plan to use[^](notes/Compute.md#app-service-plans)
* Design Web Apps for business continuity[^](notes/Compute.md#business-continuity)
* Determine when to use Azure App Service Environment (ASE)[^](notes/Compute.md#azure-app-service-environment-ase)
* Design for API apps[^](notes/Compute.md#api-apps)
* Determine when to use API management service[^](notes/Compute.md#api-management-service)
* Determine when to use Web Apps on Linux[^](notes/Compute.md#web-apps-on-linux)
* Determine when to use a CDN[^](notes/Compute.md#cdn)
* Determine when to use a cache, including Azure Redis cache[^](notes/Compute.md#using-cache)

### 1.5 Create compute-intensive application 
* Design high-performance computing (HPC) and other compute-intensive applications using Azure Services[^](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/high-performance-computing)[^](https://azure.microsoft.com/en-in/solutions/high-performance-computing/#references)
* Determine when to use Azure Batch[^](https://docs.microsoft.com/en-us/azure/batch/batch-technical-overview)
* Design stateless components to accommodate scale[^](https://blogs.msdn.microsoft.com/microsoft_press/2015/05/04/from-the-mvps-application-design-going-stateless-on-azure/)
* Design lifecycle strategy for Azure Batch[^](https://docs.microsoft.com/en-us/azure/batch/batch-api-basics)

#### Notes:
 * [Azure Compute](notes/Compute.md)

## 2. Design Data Implementation (15-20%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=storage)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=databases)
### 2.1 Design for Azure Storage solutions
Determine when to use 
* Azure Blob Storage[^](https://docs.microsoft.com/en-in/azure/storage/blobs/storage-blobs-introduction) [^](https://docs.microsoft.com/en-us/azure/storage/common/storage-decide-blobs-files-disks)
* Blob tiers [^](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers)
* Azure Files [^](https://docs.microsoft.com/en-in/azure/storage/files/storage-files-introduction)
* Disks [^](https://docs.microsoft.com/en-in/azure/virtual-machines/windows/about-disks-and-vhds)
* StorSimple [^](https://docs.microsoft.com/en-us/azure/storsimple/storsimple-ova-overview)

#### Notes:
 * [Azure Storage](notes/DataStorage.md)

#### Useful links:
 * [Queues Comparision](notes/QueuesComparision.md)
 * [Microsoft Azure Storage Performance and Scalability Checklist](https://docs.microsoft.com/en-in/azure/storage/storage-performance-checklist)

### 2.2 Design for Azure Data Services
Determine when to use 
* Data Catalog[^](https://docs.microsoft.com/en-us/azure/data-catalog/data-catalog-what-is-data-catalog) [^](notes/Database.md#azure-data-catalog)
* Azure Data Factory[^](https://azure.microsoft.com/en-us/services/data-factory/) [^](notes/Database.md#azure-data-factory)
* SQL Data Warehouse[^](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/) [^](notes/Database.md#sql-data-warehouse)
* Azure Data Lake Analytics[^](https://docs.microsoft.com/en-us/azure/data-lake-analytics/data-lake-analytics-overview) [^](notes/Database.md#Azure-Data-Lake-Analytics)
* Azure Analysis Services[^](https://docs.microsoft.com/en-us/azure/analysis-services/analysis-services-overview) [^](notes/Database.md#Azure-Analysis-Services) and
* Azure HDInsight[^](https://docs.microsoft.com/en-us/azure/hdinsight/) [^](notes/Database.md#azure-hdinsight)

### 2.3 Design for relational database storage
* Determine when to use
    * Azure SQL Database[^](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-paas-vs-sql-server-iaas)
    * SQL Server Stretch Database[^](notes/Database.md#stretch-database)
* Design for scalability[^](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-scale-introduction) and features[^](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-features)
* Determine when to use 
    * Azure Database for MySQL[^](https://docs.microsoft.com/en-us/azure/mysql/overview) 
    * Azure Database for PostgreSQL[^](https://docs.microsoft.com/en-us/azure/postgresql/overview)
* Design for HA/DR, geo-replication; design a backup and recovery strategy[^](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-disaster-recovery-strategies-for-applications-with-elastic-pool)

#### Useful links:
* [Database Notes](notes/Database.md)
* [SQL Database Automated Backups](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-automated-backups)
* [Long-term backup retension upto 10 years using Azure Recovery Services vault](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-long-term-retention)
* [Business continuity overview](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-business-continuity)
* [Designing highly available services using Azure SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-designing-cloud-solutions-for-disaster-recovery)
* [Disaster recovery strategies for applications using SQL Database elastic pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-disaster-recovery-strategies-for-applications-with-elastic-pool)


### 2.4 Design for NoSQL storage
Determine when to use
* Azure Redis Cache[^](https://azure.microsoft.com/en-in/services/cache/)[^](notes/Database.md#azure-redis-cache),
* Azure Table Storage[^](https://azure.microsoft.com/en-in/services/storage/tables/) [^](notes/Database.md#azure-table-storage),
* Azure Data Lake[^](https://docs.microsoft.com/en-us/azure/data-lake-store/data-lake-store-overview) [^](notes/Database.md#azure-data-lake-store),
* Azure Search[^](https://docs.microsoft.com/en-us/azure/search/search-what-is-azure-search)[^](notes/Database.md#azure-search),
* Time Series Insights[^](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-overview) [^](notes/Database.md#azure-time-series-insights)

### 2.5 Design for CosmosDB storage [^](https://azure.microsoft.com/en-us/services/cosmos-db/)
* Determine when to use 
    * MongoDB API[^](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-introduction),
    * DocumentDB API[^](https://docs.microsoft.com/en-us/azure/cosmos-db/sql-api-introduction),
    * Graph API[^](https://docs.microsoft.com/en-us/azure/cosmos-db/graph-introduction),
    * Azure Tables API[^](https://docs.microsoft.com/en-us/azure/cosmos-db/table-introduction)
* Design for cost [^](https://docs.microsoft.com/en-us/azure/cosmos-db/key-value-store-cost), performance [^](https://docs.microsoft.com/en-us/azure/cosmos-db/partition-data), data consistency [^](https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels), availability [^](https://docs.microsoft.com/en-us/azure/cosmos-db/online-backup-and-restore), and business continuity [^](https://docs.microsoft.com/en-us/azure/cosmos-db/regional-failover)

## 3. Design Networking Implementation (15-20%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=network)
### 3.1 Design Azure virtual networks
* Design solutions that use Azure networking services[^](https://docs.microsoft.com/en-us/azure/networking/networking-overview)
* Design for load balancing using Azure Load Balancer[^](https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview) and Azure Traffic Manager[^](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview)
* Define DNS[^](https://docs.microsoft.com/en-us/azure/dns/dns-overview), DHCP, and IP strategies
* Determine when to use Azure Application Gateway[^](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-introduction)
* Determine when to use multi-node application gateways, Traffic Manager and load balancers

### 3.2 Design external connectivity for Azure Virtual Networks
* Determine when to use Azure VPN, ExpressRoute[^](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-introduction) and Virtual Network Peering architecture and design
* Determine when to use User Defined Routes (UDRs)[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview)
* Determine when to use VPN gateway site-to-site failover for ExpressRoute[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/hybrid-networking/expressroute-vpn-failover)

### 3.3 Design security strategies
* Determine when to use network virtual appliances[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-scenario-udr-gw-nva)[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/dmz/nva-ha)[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/hybrid-networking/considerations)
* Design a perimeter network (DMZ)[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/dmz/secure-vnet-dmz)[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/dmz/)[^](https://docs.microsoft.com/en-us/azure/best-practices-network-security)
* Determine when to use a Web Application Firewall (WAF)[^](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-introduction#web-application-firewall), Network Security Group (NSG)[^](https://docs.microsoft.com/en-us/azure/virtual-network/security-overview#network-security-groups), and virtual network service tunneling[^](https://docs.microsoft.com/en-us/azure/security/azure-security-network-security-best-practices)

### 3.4 Design connectivity for hybrid applications
* Design connectivity to on-premises data from Azure applications using Azure Relay Service[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-hybrid-connections),
 Azure Data Management Gateway for Data Factory[^](https://docs.microsoft.com/en-in/azure/data-factory/v1/data-factory-data-management-gateway), Azure On-Premises Data Gateway[^](https://docs.microsoft.com/en-us/azure/analysis-services/analysis-services-gateway), Hybrid Connections[^](https://docs.microsoft.com/en-in/azure/app-service/app-service-hybrid-connections), or Azure Web App’s virtual private network (VPN) capability[^](https://docs.microsoft.com/en-us/azure/app-service/environment/network-info)
* Identify constraints for connectivity with VPN[^](https://docs.microsoft.com/en-in/azure/architecture/reference-architectures/hybrid-networking/vpn)
* Identify options for joining VMs to domains[^](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-networking)

#### Useful links:
 * [Networking Notes](notes/Networking.md)
 * [VPN Gateway FAQ](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-vpn-faq)

## 4. Design Security and Identity Solutions (20-25%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=security)
### 4.1 Design an identity solution
* Design AD Connect synchronization[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect); 
* Design federated identities using Active Directory Federation Services (AD FS)[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-azure-adfs);
* Design solutions for Multi-Factor Authentication (MFA)[^](https://docs.microsoft.com/en-us/azure/multi-factor-authentication/); 
* Design an architecture using Active Directory on-premises and Azure Active Directory (AAD)[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect); 
* Determine when to use Azure AD Domain Services[^](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-overview); 
* Design security for Mobile Apps using AAD[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-authentication-overview)[^](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-scenarios)

#### Notes:
* [Azure AD Notes](notes/AzureAD.md)
* [Security and Identity Notes](notes/NotesS&I.md)
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

#### Note: The Azure SQL Database service is only available through TCP port 1433.

#### Useful Links :
* [Azure Database Security Best Practices](https://docs.microsoft.com/azure/security/azure-database-security-best-practices)
* [Determine hybrid identity lifecycle adoption strategy](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-hybrid-identity-design-considerations-lifecycle-adoption-strategy)

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
Determine when to use the appropriate
* Cognitive Services[^](https://azure.microsoft.com/en-us/services/cognitive-services/)[^](notes/PlatformServices.md#cognitive-services)
* Azure Bot Service[^](https://docs.microsoft.com/en-in/azure/bot-service/)[^](notes/PlatformServices.md#azure-bot-service)
* Azure Machine Learning[^](https://docs.microsoft.com/en-us/azure/machine-learning/)[^](notes/PlatformServices.md#azure-machine-learning)

and other categories that fall under cognitive AI

### 5.2 Design for IoT[^](https://docs.microsoft.com/en-in/azure/iot-fundamentals/iot-introduction)
Determine when to use 
* Stream Analytics[^](https://azure.microsoft.com/en-us/services/stream-analytics/)[^](notes/PlatformServices.md#azure-stream-analytics)
* IoT Hubs[^](https://azure.microsoft.com/en-us/services/iot-hub/)[^](notes/PlatformServices.md#iot-hub)
* Event Hubs[^](https://azure.microsoft.com/en-us/services/event-hubs/)[^](notes/PlatformServices.md#event-hub)
* real-time analytics[^]()
* Time Series Insights[^](https://azure.microsoft.com/en-us/services/time-series-insights/)[^](notes/Database.md#azure-time-series-insights)
* IoT Edge[^](https://azure.microsoft.com/en-us/services/iot-edge/)[^](notes/PlatformServices.md#iot-edge)
* Notification Hubs[^](https://docs.microsoft.com/en-in/azure/notification-hubs/)[^](notes/PlatformServices.md#notification-hub)
* Event Grid[^](https://azure.microsoft.com/en-us/services/event-grid/)[^](notes/PlatformServices.md#event-grid)

and other categories that fall under IoT[^](https://azure.microsoft.com/en-us/product-categories/iot/)
### 5.3 Design messaging solution architectures
* Design a messaging architecture [^](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/messaging)
* determine when to use 
    * Azure Storage Queues[^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-azure-and-service-bus-queues-compared-contrasted)
    * Azure Service Bus[^](https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview)[^](https://docs.microsoft.com/en-us/azure/service-bus-messaging/)
    * Azure Event Hubs[^](notes/PlatformServices.md#event-hub)[^](https://docs.microsoft.com/en-us/azure/event-hubs/)
    * Event Grid[^](notes/PlatformServices.md#event-grid)[^](https://docs.microsoft.com/en-us/azure/event-grid/)
    * Azure Relay[^](notes/PlatformServices.md#azure-relay)
    * Azure Functions[^](https://azure.microsoft.com/en-in/services/functions/)[^](https://docs.microsoft.com/en-in/azure/azure-functions/functions-twitter-email)
    * Azure Logic Apps[^](https://docs.microsoft.com/en-us/azure/event-grid/compare-messaging-services)[^](https://azure.microsoft.com/en-in/blog/events-data-points-and-messages-choosing-the-right-azure-messaging-service-for-your-data/)[^](notes/QueuesComparsion.md)
* design a push notification strategy for Mobile Apps [^](https://docs.microsoft.com/en-us/azure/notification-hubs/notification-hubs-enterprise-push-notification-architecture)
* design for performance[^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-performance-improvements) and scale[^](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/performance-scalability)
### 5.4 Design for media service solutions
Define solutions using Azure Media Services[^](https://docs.microsoft.com/en-in/azure/media-services/media-services-overview), video indexer[^](https://docs.microsoft.com/en-in/azure/cognitive-services/video-indexer/video-indexer-overview), video API, computer vision API[^](https://azure.microsoft.com/en-in/services/cognitive-services/computer-vision/), preview, and other media related services

#### Notes:
* [Azure Platform Services](notes/PlatformServices.md)

## 6. Design for Operations (10-15%)[^](https://docs.microsoft.com/en-us/azure/#pivot=products&panel=mgmt)
### 6.1 Design an application monitoring and alerting strategy
* Determine the appropriate Microsoft products and services for monitoring applications on Azure [^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview)
* Define solutions for analyzing logs and enabling alerts using Azure Log Analytics[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-overview)
* Define solutions for analyzing performance metrics and enabling alerts using Azure Monitor[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor/) 
* Define a solution for monitoring applications and enabling alerts using Application Insights[^](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-overview)

### 6.2 Design a platform monitoring and alerting strategy
* Determine the appropriate Microsoft products and services for monitoring Azure platform solutions; define a monitoring solution using Azure Health[^](https://docs.microsoft.com/en-us/azure/service-health/), Azure Advisor[^](https://azure.microsoft.com/en-us/services/advisor/), and Activity Log[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-activity-logs)
* Define a monitoring solution for Azure Networks using Log Analytics[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-azure-networking-analytics) and Network Watcher service[^](https://azure.microsoft.com/en-us/services/network-watcher/)
* Monitor security with Azure Security Center[^](https://docs.microsoft.com/en-us/azure/security-center/)
### 6.3 Design an operations automation strategy
* Determine when to use Azure Automation[^](https://azure.microsoft.com/en-us/services/automation/)[^](notes/Operations.md#azure-automation), Chef[^](notes/Operations.md#chef), Puppet[^](https://puppet.com/products/managed-technology/microsoft-windows-azure)[^](notes/Operations.md#puppet), PowerShell[^](https://docs.microsoft.com/en-in/powershell/dsc/overview)[^](notes/Operations.md#powershell), Desired State Configuration (DSC)[^](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-overview)[^](notes/Operations.md#desired-state-configuration-), Event Grid[^](https://azure.microsoft.com/en-us/services/event-grid/)[^](notes/Operations.md#azure-event-grid), and Azure Logic Apps[^](https://azure.microsoft.com/en-us/services/logic-apps/)[^](notes/Operations.md#azure-logic-apps);
* Define a strategy for auto-scaling[^](https://azure.microsoft.com/en-us/features/autoscale/)[^](notes/Operations.md#azure-autoscale);
* Define a strategy for enabling periodic processes and tasks[^](https://docs.microsoft.com/en-us/azure/scheduler/scheduler-intro)[^](notes/Operations.md#azure-scheduler)

#### Notes:
* [Monitoring and Alerting, Operations Automation](notes/Operations.md)

#### Useful links
* [Avail free training](https://azure.microsoft.com/en-us/training/learning-paths/azure-solution-architect/)
* [Books to study](https://buildazure.com/2018/02/01/book-exam-ref-70-535-architecting-microsoft-azure-solutions/) [^](http://amzn.to/2Fsg5IG)
* [Azure Services](https://azure.microsoft.com/en-in/services/)
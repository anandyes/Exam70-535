## Application Monitoring and Alerting strategy

![Components that work together to provide monitoring of Azure resources](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/media/monitoring-overview/monitoring-products-overview.png)

### Monitoring Azure applications and resources

Components that work together to provide monitoring of Azure resources:
* Deep Application Monitoring - Application Insights
* Deep Infrastructure Monitoring 
    * Log Analytics
    * Management Solutions
    * Network Monitoring
    * Service Map
* Core Monitoring
    * Azure Monitor
    * Advisor
    * Service Health
    * Activity Log
* Shared Capabilities
    * Alerts
    * Dashboards
    * Metrics Explorer

### Azure Monitor[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)

* Azure Monitor helps you track performance, maintain security, and identify trends.
* Azure Monitor provides base-level infrastructure metrics and logs for most services in Microsoft Azure
* Monitor Page shows the following:
    * Triggered alerts and alert sources
    * Activity Log Errors
    * Azure Service Health
    * Application Insights
* Route - stream monitoring data to Application Insight or Event Hubs
* Store and Archive
    * Metrics - 90 days
    * Activity Log - 90 days
    * Diagnostics logs are not stored.

### Azure Log Analytics[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-overview)
Log Analytics plays a central role in Azure management by collecting telemetry and other data from a variety of sources and providing a query language and analytics engine that gives you insights into the operation of your applications and resources.

* Log Analytics includes a rich query language to quickly retrieve, consolidate, and analyze collected data
* Views in Log Analytics visually present data from log searches.

### Application Insights[^](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-overview)
* Application Insights is an extensible Application Performance Management (APM) service for web developers on multiple platforms.
* It can monitor and analyze telemetry from mobile apps by integrating with Visual Studio App Center and HockeyApp.

## Monitoring Azure Platform and Alerting

Azure Monitor enables core monitoring for Azure services by allowing the collection of metrics, activity logs, and diagnostic logs. 

### Azure Service Health[^](https://docs.microsoft.com/en-us/azure/service-health/)

* Azure Service Health can notify you, help you understand the impact of issues, and keep you updated as the issue resolves.
* Prepare for planned maintenance and changes that could affect the availability of your resources.
* Components of Azure Health:
    * Azure Status - a global view of health of Azure services, real time status updates and history pages
    * Service Health - a personalized view of health of Azure services, provides a customizable dashboard. Tracks 3 types of health events:
        * Serviec issues (any ongoing problems)
        * Planned maintenance
        * Health advisories
    * Resource Health - a deeper view of the health of the individual resources provisioned to you by your Azure services, provides technical support to help you mitigate problems. Resource Health statuses are:
        * Available
        * Unavailable
        * Non-platform events - triggered by users' actions
        * Unknown - no update since 10 mins
        * Degraded - detected a loss in performance

### Azure Advisor[^](https://docs.microsoft.com/en-us/azure/advisor/advisor-overview)
* Advisor is a personalized cloud consultant that helps to follow best practices to optimize Azure deployments.
* constantly monitors your resource configuration and usage telemetry.
* Get proactive, actionable, and personalized best practices recommendations
* Improve the performance, security, and high availability of your resources, as you identify opportunities to reduce your overall Azure spend
* Get recommendations with proposed actions inline. 
* Categories of recomendation:
    * High Availability
    * Security
    * Performance
    * Cost
* Advisor provides recommendations for virtual machines, availability sets, application gateways, App Services, SQL servers, and Redis Cache.

### Activity Log[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-activity-logs)
* Provides data about the operation of an Azure resource
* Is a subscription log that provides insight into subscription-level events that have occurred in Azure
* Primarily for ARM activities, does not track resources using the Classic/RDFE model
* The Activity Log was previously known as “Audit Logs” or “Operational Logs
* Categories of data in Activity Log: 
    * Administrative - Resource Manager operations
    * Service Health - events: Action Required, Assisted Recovery, Incident, Maintenance, Information, or Security
    * Alert - record of activation of Azure alerts
    * Autoscale - events related to the operation of the autoscale engine
    * Recommendation - events offer recommendations for how to better utilize your resources
    * Security - alerts generated by Azure Security Center
    * Policy and Resource Health - reserved for future use

### Diagnostics Logs[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-of-diagnostic-logs)
* Resource-level diagnostic logs provide insight into operations that were performed within that resource itself.
* Resource-level diagnostic logs differ from the Activity Log and guest OS-level diagnostic logs
* Activity Log provides insight into the operations that were performed on resources.
* Guest OS diagnostic logs are those collected by an agent running inside of a virtual machine or other supported resource type.
* Resource-level diagnostic logs require no agent and capture resource-specific data from the Azure platform itself, while guest OS-level diagnostic logs capture data from the operating system and applications running on a virtual machine.

### Monitoring Azure Networks

Log Analytics offers the following solutions for monitoring your networks:
* Network Perfomance Monitor (NPM) - to monitor health of your network
* Azure Application Getway analytics to review
    * Azure Application Gateway logs
    * Azure Application Gateway metrics
* Solutions to monitor and audit network activity on your cloud network
* Traffic Analytics[^](https://docs.microsoft.com/azure/networking/network-monitoring-overview#traffic-analytics)
* Azure Network Security Group Analytics

Network Performance Monitor (NPM) [^](https://docs.microsoft.com/en-in/azure/networking/network-monitoring-overview)
* NPM management solution is a network monitoring solution, that monitors the health, availability and reachability of networks.
* It is used to monitor connectivity between:
    * Public cloud and on-premises
    * Data centers and user locations (branch offices)
    * Subnets hosting various tiers of a multi-tiered application.
* Network Performance Monitor detects network issues like traffic blackholing, routing errors, and issues that conventional network monitoring methods aren't able to detect
* NPM is a cloud-based hybrid network monitoring solution that helps you monitor network performance between various points in your network infrastructure
* Network Performance Monitor offers three broad capabilities:
    * Performance Monitor[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-network-performance-monitor-performance-monitor)
    * Service Endpoint Monitor[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-network-performance-monitor-service-endpoint)
    * ExpressRoute Monitor[^](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-network-performance-monitor-expressroute)

Azure Application Gateway and Network Security Group analytics  management solutions collect diagnostics logs directly from Azure Application Gateways and Network Security Groups.

Network Watcher Service[^](https://azure.microsoft.com/en-us/services/network-watcher/)
* Network Watcher is a regional service that enables you to monitor and diagnose conditions at a network scenario level in, to, and from Azure.
* Automate remote network monitoring with packet capture
* Gain insight into your network traffic using flow logs
* Diagnose VPN connectivity issues
* Capabilities:
    * Topology
    * Variable Packet Capture
    * IP flow verify
    * Next Hop
    * Security group view
    * NSG flow logging
    * VNet Gateway and Connection troubleshooting
    * Network subscription limits
    * Configuring Diagnostics log
    * Connection troubleshoot
    * Connection Monitor
* Network Watcher uses RBAC model

### Monitor security with Azure Security Center[^](.\SecurityCenter.md)[^](https://docs.microsoft.com/en-us/azure/security-center/security-center-network-recommendations)
* Azure Security Center provides unified security management and advanced threat protection across hybrid cloud workloads.
* Security Center identifies potential security vulnerabilities, it creates recommendations that guide you through the process of configuring the needed controls
* Available network recommendations:
    * Add a Next Generation Firewall (NGFW)
    * Route traffic through NGFW only
    * Enable Network Security Groups on subnets or virtual machines
    * Restrict access through Internet facing endpoint
* Integrated Azure Security solutions
    * Endpoint protection (Trend Micro, Symantec, Windows Defender, and System Center Endpoint Protection (SCEP))
    * Web application firewall (Barracuda, F5, Imperva, Fortinet, and Azure Application Gateway)
    * Next-generation firewall (Check Point, Barracuda, Fortinet, and Cisco)
    * Vulnerability assessment (Qualys) 

## Operations Automation Strategy

### Azure Automation[^](https://docs.microsoft.com/en-us/azure/automation/automation-intro)
* Azure Automation delivers a cloud-based automation and configuration service that provides consistent management across your Azure and non-Azure environments
* It consists of process automation, update management, and configuration features.
* Azure Automation provides complete control during deployment, operations, and decommissioning of workloads and resources
* Azure Automation capabilities:
    * Process Automation: Orchestrate processes using graphical, Powershell, and Python runbooks
    * Configuration management: Collect inventory, track changes, configure desired state
    * Update management: Assess compliance, Schedule update installation across hybrid environments
    * Heterogeneous: Windows & Linux, Azure and on-premises
    * Shared Capabilities: RBAC, Secure, global store for variables, credentials, certificates,connections. Flexible Scheduling, Shared modules, Source Control support, Auditing, Tags
* When to use Azure Automation:
    * if you do not already have a Configuration Management Solution, or not deeply embedded
    * If you want to significantly expand your configuration management without significant expense
    * If you already own OMS
    * If you already have PowerShell expertise

### Chef[^](https://docs.microsoft.com/en-in/azure/virtual-machines/windows/chef-automation?toc=%2Fazure%2Fvirtual-machines%2Fwindows%2Ftoc.json)
* Chef has three main architectural components: Chef Server, Chef Client (node), and Chef Workstation.
* Cross-OS systems management, automation and analytics output
* Ruby and Git are required plus agent is on target machine
* Good development focused teams (code driven approach to configuration)
* Leverage Chef in Azure when already using it.
* When to use Chef:
    * If you already have a Chef management infrastructure
    * If your primary expertise is managing Linux machines

### Puppet[^](https://blogs.technet.microsoft.com/lukeb/2016/02/05/azure-puppet-on-premises-deploying-to-azure/)[^](https://azure.microsoft.com/en-us/blog/azure-virtual-machines-using-chef-puppet-and-docker-for-managing-linux-vms/)
* Puppet - is an Open Source configuration management system that allows you to define the state of your IT infrastructure, then automatically enforces the correct state.
* Stable and mature so good for managing large, heterogeneous enterprise environments
* Automate systems configuration and enforce consitency
* Large Open Source catalog of modules and runs on nearly every OS (cross platform)
* When to use Puppet:
    * If you already have a Puppet management infrastructure
    * If your primary expertise is managing Linux machines

### PowerShell[^](https://docs.microsoft.com/en-in/powershell/azure/overview?view=azurermps-5.7.0)[^](https://docs.microsoft.com/en-in/powershell/dsc/overview)
* Azure PowerShell provides a set of cmdlets that use the Azure Resource Manager model for managing your Azure resources.
* Use the Cloud Shell to run the Azure PowerShell in your browser or install it on own computer
* PowerShell supports asynchronous action with PowerShell Jobs.
* PowerShell background jobs run a command or expression in the background without interacting with the current session.
* Azure PowerShell also provides an -AsJob switch on some long-running cmdlets
* DSC is a management platform in PowerShell that enables you to manage your IT and development infrastructure with configuration as code
* DSC is a declarative platform used for configuration, deployment, and management of systems.
* Three primary components:
    * Configurations - are declarative PowerShell scripts which define and configure instances of resources
    * Resources - A resource exposes properties that can be configured (schema) and contains the PowerShell script functions that LCM calls
    * Local Configuration Manager (LCM) - is the engine by which DSC facilitates the interaction between resources and configurations.

### Desired State Configuration (DSC)[^](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-overview)
* Azure Automation DSC is an Azure service that allows you to write, manage, and compile PowerShell Desired State Configuration (DSC) configurations, import DSC Resources, and assign configurations to target nodes, all in the cloud.
* Azure Automation DSC provides several advantages over using DSC outside of Azure:
    * Built-in pull server - target nodes automatically receive configurations, conform to the desired state, and report back on their compliance.
    * Management of all your DSC artifacts
    * Import reporting data into Log Analytics
* Install or remove windows roles and features
* Running Windows PowerShell scripts
* Managing registry settings
* Managing files and directories
* Starting, stopping and managing processes and services
* Managing groups and user accounts
* Deploying new software
* Manging environment variables
* Discovering the actual configuration state on a given node
* Fixing a configuration that has drifted away from the desired state
* When to use DSC:
    * If you do not already have a Configuration Mangement Solution
    * If your primary experience is in managing Windows machines
    * Uses vendor-neutral configuration files (MOF)
    * If you already have PowerShell expertise

### Azure Event Grid[^](./PlatformServices.md#event-grid)
* Fully managed event routing
* Near real-time event delivery at scale
* Broad coverage within Azure and beyond
* backbone of event-driven computing
* Manage all events at one place
* Scenarios
    * Serverless apps
    * Ops Automation - notify Azure automation when underlying infrastructure is provisioned
    * Application integration

### Azure Logic Apps[^](https://docs.microsoft.com/en-us/azure/logic-apps/)
* Azure Logic Apps simplifies how you build automated scalable workflows that integrate apps and data across cloud services and on-premises systems.
* Logic Apps helps you build, schedule, and automate processes as workflows so you can integrate apps, data, systems, and services across enterprises or organizations
* Every logic app workflow starts with a trigger, which fires when a specific event happens, or when new available data meets specific criteria.

### Azure Autoscale[^](https://azure.microsoft.com/en-us/features/autoscale/)[^](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-overview-autoscale)
* Autoscale is a built-in feature of Cloud Services, Mobile Services, Virtual Machines, and Websites that helps applications perform their best when demand changes
* Autoscale allows you to have the right amount of resources running to handle the load on your application.
*  It allows you to add resources to handle increases in load and also save money by removing resources that are sitting idle.

### Azure Scheduler[^](https://docs.microsoft.com/en-us/azure/scheduler/scheduler-intro)
* Azure Scheduler allows you to declaratively describe actions to run in the cloud. It then schedules and runs those actions automatically.
* It invokes via HTTP, HTTPS, a storage queue, a service bus queue, or a service bus topic.
* Recurring application actions - Periodically gathering data from Twitter into a feed
* Daily maintenance - Daily pruning of logs, performing backups, and other maintenance tasks
* Scheduler allows you to create, update, delete, view, and manage jobs and job collections programmatically, by using scripts, and in the portal.
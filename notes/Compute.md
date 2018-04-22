## Virtual Machines
 availability sets, fault domains, and update domains
 web app for containers
 VM Scale Sets
 compute-intensive tasks using Azure Batch
 migration strategy from cloud services
 Azure Backup
 Azure Site Recovery

## Serverless Computing
Azure Functions, event-driver
Azure Container Instances
Azure Logic Apps and Azure Functions
API Management Service

## Microservices
container-based solution
container-orchestration
Azure Service Fabric (ASF) 
Azure Functions
Web API
platform for container orchestration
migrating existing assets versus cloud native deployment
lifecycle management strategies

## Web Applications
[ASP.NET Overview](https://docs.microsoft.com/en-us/aspnet/overview)

### Azure App Service Web Apps[^](https://docs.microsoft.com/en-us/azure/app-service/app-service-web-overview)
Azure App Service Web Apps (or just Web Apps) is a service for hosting web applications, REST APIs, and mobile back ends.

Key features of App Service Web Apps:
* Multiple languages and frameworks support
* DevOps optimization - CI/CD, staging, PowerShell, CLI
* Global scale with high availability - Scale up or Out
* Connections to SaaS platforms and on-premises data - more than 50 connetors, Hybrid connections, and Azure VNets
* Security and Compliance - ISO, SOC and PCI compliant, Authenticate using AAD, or social login. IP restrictions (Firewall), manage service Identities
* Application templates
* Visual Studio Integration
* API and mobile features
* Serverless code

### Custom Web API[^](https://docs.microsoft.com/en-in/azure/logic-apps/logic-apps-create-api-app)
* Custom APIs and custom connectors are web APIs that use REST for pluggable interfaces, Swagger metadata format for documentation, and JSON as their data exchange format. 
* A custom API works best with logic apps when the API also has a Swagger document that describes the API's operations and parameters.
* Custom API should provide actions. A basic action is a controller that accepts HTTP requests and returns HTTP responses.
* Action Patterns
    * Perform long-running tasks with the **polling action pattern**
    * Perform long-running tasks with the **webhook action pattern**
* Trigger patterns
    * Check for new data or events regularly with the **polling trigger pattern**
    * Wait and listen for new data or events with the **webhook trigger pattern**

[On-Premises PowerBI Gateway](https://docs.microsoft.com/en-in/power-bi/service-gateway-getting-started)
A gateway is software that facilitates access to data that resides on a private, on-premises network, for subsequent use in a cloud service like Power BI.


### Secure Web API [^](https://docs.microsoft.com/en-us/aspnet/web-api/overview/security/)[^](https://docs.microsoft.com/en-in/azure/logic-apps/logic-apps-custom-api-authentication)
* Authentication and Authorization in Web API
    * *Authentication* is knowing the identity of the user
    * *Authorization* is deciding whether a user is allowed to perform an action
    * Web API assumes that authentication happens in the host(IIS), IIS uses HTTP modules for authentication.
    * Alernatively, authentication logic can be put into an HTTP message handler
    * Authorization happens later in the pipeline, closer to the controller.
    * Authorization filters run before the controller action
    * Web API provides a built-in authorization filter, **AuthorizeAttribute**.
    
* Secure a Web API with Individual Accounts in Web API 2.2
    * Secure a web API using OAuth2 to authenticate against a membership database
    * Web API project template gives you three options for authentication:
        * Individual accounts. The app uses a membership database.
        * Organizational accounts. Users sign in with their Azure Active Directory, Office 365, or on-premise Active Directory credentials.
        * Windows authentication. This option is intended for Intranet applications, and uses the Windows Authentication IIS module.
    * Individual accounts provide two ways for a user to log in:
        * Local Login - The user registers at the site
        * Social Login - The user signs in with external social media account
    * For both local and social login, Web API uses OAuth2 to authenticate requests
* External Authentication Services with Web API (C#)
    * to integrate with external authentication services, which include several OAuth/OpenID and social media authentication services: Microsoft Accounts, Twitter, Facebook, and Google.

* Preventing Cross-Site Request Forgery (CSRF) Attacks in Web API
    * Cross-Site Request Forgery (CSRF) is an attack where a malicious site sends a request to a vulnerable site where the user is currently logged in
    * Using SSL does not prevent a CSRF attack, because the malicious site can send an "https://" request.
    * CSRF attacks are possible against web sites that use cookies for authentication, because browsers send all relevant cookies to the destination web site. Basic and Digest authentication are also vulnerable
    * To help prevent CSRF attacks, ASP.NET MVC uses anti-forgery tokens, also called request verification tokens.
    * Same-origin policies prevent documents hosted on two different sites from accessing each other's content
* Enabling Cross-Origin Requests in Web API 2
    * Browser security prevents a web page from making AJAX requests to another domain. This restriction is called the same-origin policy, and prevents a malicious site from reading sensitive data from another site. 
    * Cross Origin Resource Sharing (CORS) is a W3C standard that allows a server to relax the same-origin policy. 
    * Using CORS, a server can explicitly allow some cross-origin requests while rejecting others.
* Authentication Filters in Web API 2
    * An authentication filter is a component that authenticates an HTTP request
    * Authentication filters let you set an authentication scheme for individual controllers or actions.
    * authentication filters can be applied per-controller, per-action, or globally to all Web API controllers.
    * "Host-level authentication" is authentication performed by the host (such as IIS), before the request reaches the Web API framework.
    * [Web API Security Filter](https://msdn.microsoft.com/magazine/dn781361.aspx) (MSDN Magazine)
* Basic Authentication in Web API
    * Basic authentication is performed within the context of a "realm."
    * The credentials are sent unencrypted, Basic authentication is only secure over HTTPS.
    * Basic authentication is also vulnerable to CSRF attacks
* Forms Authentication in Web API
    * Forms authentication uses an HTML form to send the user's credentials to the server.
    * Forms authentication is only appropriate for web APIs that are called from a web application, so that the user can interact with the HTML form.
    * Advantages:
        * Easy to implement: Built into ASP.NET.
        * Uses ASP.NET membership provider, which makes it easy to manage user accounts
    * Disadvantages:
        * Not a standard HTTP authentication mechanism;
        * uses HTTP cookies instead of the standard Authorization header.
        * Requires a browser client.
        * Credentials are sent as plaintext.
        * Vulnerable to cross-site request forgery (CSRF).
        * Requires anti-CSRF measures.
        * Difficult to use from nonbrowser clients.
        * Login requires a browser.
        * User credentials are sent in the request. Some users disable cookies.
* Integrated Windows Authentication
    * Integrated Windows authentication enables users to log in with their Windows credentials, using Kerberos or NTLM.
    * The client sends credentials in the Authorization header.
    * Windows authentication is best suited for an intranet environment
    * Windows authentication is vulnerable to cross-site request forgery (CSRF) attacks
    * Advantages:
        * Built into IIS.
        * Does not send the user credentials in the request.
        * If the client computer belongs to the domain (for example, intranet application), the user does not need to enter credentials
    * Disadvantages:
        * Not recommended for Internet applications.
        * Requires Kerberos or NTLM support in the client.
        * Client must be in the Active Directory domain.
* Working with SSL
    * Basic authentication and forms authentication send unencrypted credentials. To be secure, these authentication schemes must use SSL. 
    * In addition, SSL client certificates can be used to authenticate clients.
    * SSL provides authentication by using Public Key Infrastructure certificates
    * Advantages:
        * Certificate credentials are stronger than username/password.
        * SSL provides a complete secure channel, with authentication, message integrity, and message encryption.
    * Disadvantages:
        * must obtain and manage PKI certificates.
        * The client platform must support SSL client certificates.


### Web Apps for scalability and performance[^](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/scalable-web-app)

#### Azure App Service Local Cache[^](https://docs.microsoft.com/en-in/azure/app-service/app-service-local-cache-overview#best-practices-for-using-app-service-local-cache)
* Provides a web role view of your content. Web apps that run on Local Cache have the following benefits:
    * They are immune to latencies that occur when they access content on Azure Storage.
    * They are immune to the planned upgrades or unplanned downtimes and any other disruptions with Azure Storage that occur on servers that serve the content share.
    * They have fewer app restarts due to storage share changes.
* The local cache is a copy of the /site and /siteextensions folders of the web app.
* Use Local Cache if your web app needs a high-performance, reliable content store, that does not use the content store to write critical data at runtime, and is less than 2 GB in total size 

#### SignalR[^](https://docs.microsoft.com/en-us/aspnet/signalr/overview/getting-started/introduction-to-signalr)
* ASP.NET SignalR is a library for ASP.NET developers that simplifies the process of adding real-time web functionality to applications.
* Real-time web functionality is the ability to have server code push content to connected clients instantly as it becomes available, rather than having the server wait for a client to request new data.
* SignalR can be used to add any sort of "real-time" web functionality to your ASP.NET application.
* Examples include Chats, dashboards and monitoring applications, collaborative applications (such as simultaneous editing of documents), job progress updates, and real-time forms.
* The SignalR API contains two models for communicating between clients and servers: Persistent Connections and Hubs.
### Multi region, high availability Azure web apps[^](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/multi-region)
### App Service plans[^](https://docs.microsoft.com/en-in/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview)
### Business Continuity[^](https://docs.microsoft.com/en-us/azure/architecture/resiliency/disaster-recovery-azure-applications)
### Azure App Service Environment (ASE)[^](https://docs.microsoft.com/en-us/azure/app-service/environment/intro)
* The Azure App Service Environment is an Azure App Service feature that provides a fully isolated and dedicated environment for securely running App Service apps at high scale.

### API apps[^](https://azure.microsoft.com/en-in/services/app-service/api/)
### API management service[^](https://docs.microsoft.com/en-us/azure/api-management/api-management-key-concepts)
* API Management (APIM) helps organizations publish APIs to external, partner, and internal developers to unlock the potential of their data and services.
* The **API gateway** is the endpoint that accepts API calls and routes them to your backends.
* The **Azure portal** is the administrative interface where you set up your API program
* The **Developer portal** serves as the main web presence for developers

### Web Apps on Linux[^](https://docs.microsoft.com/en-in/azure/app-service/containers/app-service-linux-intro)
### CDN[^](https://docs.microsoft.com/en-us/azure/cdn/cdn-overview)
### Using Cache [^](https://docs.microsoft.com/en-us/azure/cdn/cdn-how-caching-works), Azure Redis Cache[^](https://azure.microsoft.com/en-in/services/cache/)

[Azure App Service, Virtual Machines, Service Fabric, and Cloud Services comparison](https://docs.microsoft.com/en-us/azure/app-service/choose-web-site-cloud-service-vm?toc=%2fazure%2fapp-service%2fcontainers%2ftoc.json)

## High Performance Computing, Compute-intensive Applications[^](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/high-performance-computing)
Azure provides flexible solutions to distribute work and scale to thousands of VMs or cores and then scale down when you need fewer resources. 

### Design High-performance computing (HPC) and other Compute-intensive applications using Azure Services


### Azure Batch
* Azure Batch creates and manages a pool of compute nodes (virtual machines), installs the applications you want to run, and schedules jobs to run on the nodes.
* There is no cluster or job scheduler software to install, manage, or scale. Instead, you use Batch APIs and tools, command-line scripts, or the Azure portal to configure, manage, and monitor your jobs.
* Intrinsically parallel workloads are those where the applications can run independently, and each instance completes part of the work
* Examples of intrinsically parallel workloads you can bring to Batch:
    * Financial risk modeling using Monte Carlo simulations
    * VFX and 3D image rendering
    * Image analysis and processing
    * Media transcoding
    * Genetic sequence analysis
    * Optical character recognition (OCR)
    * Data ingestion, processing, and ETL operations
    * Software test execution
* Tightly coupled workloads need to communicate with each other, as opposed to run independently. Tightly coupled applications normally use the Message Passing Interface (MPI) API.
* Examples of tightly coupled workloads:
    * Finite element analysis
    * Fluid dynamics
    * Multi-node AI training
* Batch supports large-scale rendering workloads with rendering tools including Autodesk Maya, 3ds Max, Arnold, and V-Ray. 
* R users can install the doAzureParallel R package to easily scale out the execution of R algorithms on Batch pools.
* Run Batch jobs as part of a larger Azure workflow to transform data, managed by tools such as Azure Data Factory.

Batch Service Resources:[^](https://docs.microsoft.com/en-in/azure/batch/batch-api-basics#batch-service-resources)

* Account
* Compute node - VM that is dedicated to processing a portion of your application's workload
* Pool - collection of nodes that your application runs on
* Job - A job is a collection of tasks
    * Job schedules - create recurring jobs
* Task - unit of computation that is associated with a job and runs on a node
    * Start task
    * Job manager task - control and/or monitor job execution
    * Job preparation and release tasks
    * Multi-instance task (MPI)
    * Task dependencies
* Application packages - provide simplified deployment and versioning of the applications that your tasks run

### Design stateless components to accommodate scale [^](https://docs.microsoft.com/en-us/azure/architecture/checklist/scalability)

* Scalability is the ability of a system to handle increased load.
* Application design:
    * Partition the workload
    * Design for scaling - the application and the services it uses must be stateless, to allow requests to be routed to any instance. 
    * Scale as a unit
    * Avoid client affinity
    * Autoscaling capability
    * Offload intensive CPU/IO tasks as background tasks
    * Distribute the workload for background tasks
    * shared-nothing architecture
* Data management
    * Use data partitioning
    * Design for eventual consistency
    * Reduce chatty interactions between components and services
    * Use queues to level the load for high velocity data writes
    * Minimize the load on the data store
    * Minimize the volume of data retrieved
    * Aggressively use caching
    * Handle data growth and retention
    * Optimize Data Transfer Objects (DTOs) using an efficient binary format
    * Set cache control
    * Enable client side caching.
    * Use Azure blob storage and the Azure Content Delivery Network to reduce the load on the application
    * Optimize and tune SQL queries and indexes
    * Consider de-normalizing data.
* Implementation[^](https://docs.microsoft.com/en-us/azure/architecture/checklist/scalability#implementation)


### Design lifecycle strategy for Azure Batch[^](https://docs.microsoft.com/en-in/azure/batch/batch-api-basics)
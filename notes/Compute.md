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
Azure App Service Web Apps
Custom Web API
Secure Web API
Web Apps for scalability and performance
Multi region, high availability Azure web apps
App Service plans
Business Continuity
Azure App Service Environment (ASE)
API apps
API management service
Web Apps on Linux
CDN
Using Cache, Azure Redis Cache

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
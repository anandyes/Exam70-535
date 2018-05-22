## Artificial Intelligence Services

### Azure Machine Learning[^](https://docs.microsoft.com/en-in/azure/machine-learning/preview/overview-what-is-azure-ml)
* Azure Machine Learning services (preview) enable building, deploying, and managing machine learning and AI models using any Python tools and libraries.
* Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends
* Azure Machine Learning Components:
    * Azure Machine Learning Workbench
    * Azure Machine Learning Experimentation Service
    * Azure Machine Learning Model Management Service
    * Microsoft Machine Learning Libraries for Apache Spark (MMLSpark Library)
    * Visual Studio Code Tools for AI
    * Other ML products [^](https://docs.microsoft.com/en-in/azure/machine-learning/preview/overview-more-machine-learning)
        * SQL Server Machine Learning Services
        * Microsoft Machine Learning Server
        * Azure Machine Learning Services
        * Azure Machine Learning Studio
        * Data Science Virtual Machine
        * Spark MLLib in HDInsight
        * Batch AI Training Service
        * Microsoft Cognitive Toolkit
        * Microsoft Cognitive Services
    * Azure Machine Learning has two types of web services:
        * Request-Response Service (RRS): A low latency, highly scalable service that provides an interface to the stateless models created and deployed by using Machine Learning Studio.
        * Batch Execution Service (BES): An asynchronous service that scores a batch for data records. 

### Azure Bot Service[^](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction)

* Bot Service provides the core components for creating bots, including the Bot Builder SDK for developing bots and the Bot Framework for connecting bots to channels.
* Two hosting plans
    * App Service plan - standard Azure web app, predictable costs and scaling
    * Consumption plan - serverless bot that runs on Azure Functions, pay-per-run pricing
* Bot Service Features:
    * Multiple language support - .NET and Node.js
    * Bot templates - Basic bot, a Forms bot, LUIS, QnA bot, Proactive bot 
    * Support dependencies - NuGet and NPM support
    * Flexible development - Azure portal, GitHub, VSTS, Visual Studio 
    * Connect to channels - Skype, Facebook, Teams, Slack, SMS etc.
    * Tools and services - Bot Framework Emulator, Channel Inspector
    * Open source - Bot Builder SDK is open-source
* Bot State service
    * Enables your bot to store and retrieve state data that is associated with a user, a conversation, or a specific user within the context of a specific conversation.
    * REST and JSON over HTTPS
    * authentication with JWT Bearer tokens

### Cognitive Services[^](https://azure.microsoft.com/en-us/services/cognitive-services/)
Infuse your apps, websites and bots with intelligent algorithms to see, hear, speak, understand and interpret your user needs through natural methods of communication

* Vision
    * Computer Vision API
    * Face API
    * Content Moderator
    * Emotion API
    * Custom Vision Service 
    * Video Indexer
* Speech
    * Translator Speech API 
    * Speaker Recognition API 
    * Bing Speech API
    * Custom Speech Service
* Knowledge
    * QnA Maker API
    * Custom Decision Service
* Language
    * Language Understanding (LUIS)
    * Text Analytics API 
    * Bing Spell Check API 
    * Translator Text API
    * Web Language Model API
    * Linguistic Analysis API
* Search
    * Bing Autosuggest API
    * Bing Image Search API
    * Bing News Search API
    * Bing Video Search API
    * Bing Web Search API
    * Bing Custom Search API
    * Bing Entity Search API

## Azure IoT

### Azure Stream Analytics[^](https://docs.microsoft.com/en-us/azure/stream-analytics/)
* Azure Stream Analytics is a managed event-processing engine set up real-time analytic computations on streaming data
* The data can come from devices, sensors, web sites, social media feeds, applications, infrastructure systems, and more
* Use Stream Analytics to examine high volumes of data streaming from devices or processes, extract information from that data stream, identify patterns, trends, and relationships.
* The data can be ingested into Azure from a device using an Azure event hub or IoT hub. The data can also be pulled from a data store like Azure Blob Storage.
* Stream Analytics can handle up to 1 GB of incoming data per second
* Response to analysis:
    * Send a command to change device settings. 
    * Send data to a monitored queue for further action based on findings (such as event hubs, Azure Service Bus, queues)
    * Send data to a Power BI dashboard.
    * Send data to storage like Data Lake Store, Azure SQL Database, or Azure Blob storage.
* Stream Analytics provides a SQL-like language for creating transformations (SQL DSL)
* Azure provides multiple solutions for analyzing streaming data: Azure Streaming Analytics and Apache Storm on Azure HDInsight
* Stream Analytics pricing is based on volume of data processed and the number of streaming units required per hour that the job is running
* Apache Storm on HDInsight pricing is cluster-based, and is charged based on the time the cluster is running, independent of jobs deployed
* Stream Analytics enables developers to use Tumbling, Hopping and Sliding windows to perform temporal operations on streaming data

### IoT Hub[^](https://docs.microsoft.com/en-us/azure/iot-hub/)[^](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-what-is-iot-hub)
Azure IoT Hub is a fully managed service that enables reliable and secure bidirectional communications between millions of IoT devices and a solution back end

Comparision between IoT Hub and Event Hub[^](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-compare-event-hubs)

|||||
|:--|:--|:--|:--|
| IoT Capability | IoT Hub standard tier | IoT Hub basic tier | Event Hubs |
| Device-to-cloud messaging | Yes | Yes | Yes |
| Protocols: HTTPS, AMQP, AMQP over websockets | Yes | Yes | Yes |
| Protocols: MQTT, MQTT over websockets | Yes | Yes | |
| Per-device identity | Yes | Yes | |
| File upload from devices | Yes | Yes | |
| Device Provisioning Service | Yes | Yes | |
| Cloud-to-device messaging | Yes | | |
| Device twin and device management | Yes | | |
| IoT Edge | Yes | | |
|||||

IoT Hub communication options: 
* Device Twins
* Per-device authentication and secure connectivity
* Route device-to-cloud messages to Azure services based on declarative rules
* Integrate IoT Hub events into your business applications: IoT Hub integrates with Azure Event Grid
* Monitoring of device connectivity operations
* An extensive set of device libraries
* IoT protocols and extensibility: enables devices to natively use the MQTT v3.1.1, HTTPS 1.1, or AMQP 1.0 protocols
* Scale
* Device provisioning

Gateways:
* A protocol gateway performs protocol translation, for example MQTT to AMQP
* A field gateway can:
    * Run analytics on the edge.
    * Make time-sensitive decisions to reduce latency.
    * Provide device management services.
    * Enforce security and privacy constraints.
    * Perform protocol translation.
* A field gateway differs from a simple traffic routing device (NAT / firewall)

### Event Hub[^](https://docs.microsoft.com/en-in/azure/event-hubs/event-hubs-what-is-event-hubs)
* Azure Event Hubs is a highly scalable data streaming platform and event ingestion service, capable of receiving and processing millions of events per second.
* Data sent to an event hub can be transformed and stored using any real-time analytics provider or batching/storage adapters
* Event Hub is different from Azure Service Bus messaging, and does not implement some of the capabilities that are available for Service Bus messaging entities, such as topics.

Event Hubs features:
* Event producers/publishers: An event is published via AMQP 1.0 or HTTPS
* Capture
* Partitions: Enables each consumer to only read a specific subset, or partition, of the event stream
* Event consumers
* Consumer groups
* Throughput units: Throughput units are pre-purchased units of capacity
* Billing plan: Basic, Standard, Dedicated

### Time Series Insights[^](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-overview)[^](notes/Database.md#azure-time-series-insights)

### IoT Edge[^]()
* Azure IoT Edge moves cloud analytics and custom business logic to devices
* Azure IoT Edge is only available in the standard tier of IoT Hub
* Azure IoT Edge is made up of three components:
    * IoT Edge modules - Docker compatible containers that run Azure services, 3rd party services, code
    * IoT Edge runtime - runs on IoT edge device and manages modules deployed, Supports both Linux and Windows OS
    * IoT Edge cloud interface - to configure workloads, monitor and manage IoT Edge devices

### Notification Hub[^](https://docs.microsoft.com/en-in/azure/notification-hubs/notification-hubs-push-notification-overview)
* Azure Notification Hubs provide an easy-to-use, multi-platform, scaled-out push engine.
* a single cross-platform API call to send targeted and personalized push notifications to any mobile platform from any cloud or on-premises backend
* Push notifications is a form of app-to-user communication where users of mobile apps are notified of certain desired information, usually in a pop-up or dialog box
* Push notifications are delivered through platform-specific infrastructures called Platform Notification Systems (PNSes)
* Notification Hubs is offered in three tiers—free, basic and standard. Base charge and quotas are applied at the namespace level[^](https://azure.microsoft.com/en-in/pricing/details/notification-hubs/)

Challenges of Push Notifications:
* Platform dependency
* Scale - device tokens must be refreshed upon every app launch, broadcast support
* Routing - backend must maintain a registry to associate devices with interest groups, users, properties, etc.

Notification Hub advantages:
* Cross platforms - iOS, Android, Windows, and Kindle and Baidu
* Cross backends - Cloud or on-premises, .NET, Node.js, Java, etc
* Rich set of delivery patterns:
    * Broadcast to one or multiple platforms
    * Push to device
    * Push to user
    * Push to segment with dynamic tags
    * Localized push
    * Silent push
    * Scheduled push
    * Direct push
    * Personalized push
* Rich telemetry
* Scalability
* Security - SAS or federated authentication

 App Service Mobile Apps has built-in support for push notifications using Notification Hubs.

### Event Grid[^](https://docs.microsoft.com/en-in/azure/event-grid/overview)
![Event Grid Functional Model](https://docs.microsoft.com/en-us/azure/event-grid/media/overview/functional-model.png)
* Event Grid is a fully managed event routing service which provides reliable message delivery at massive scale
* Azure Event Grid is a fully-managed intelligent event routing service that allows for uniform event consumption using a publish-subscribe mode
* Azure Event Grid allows you to easily build applications with event-based architectures
* Event Grid has built-in support for events coming from Azure services, like storage blobs and resource groups
* Event sources (Topics)
    * Azure Subscriptions (management operations)
    * Custom Topics
    * Event Hubs
    * IoT Hub
    * Resource Groups (management operations)
    * Service Bus
    * Storage Blob
    * Storage General-purpose v2 (GPv2)
* Event handlers
    * Azure Automation
    * Azure Functions
    * Event Hubs
    * Logic Apps
    * Microsoft Flow
    * WebHooks
* When using Azure Functions as the handler, use the Event Grid trigger instead of generic HTTP triggers. Event Grid automatically validates Event Grid Function triggers. With generic HTTP triggers, you must implement the validation response.
* Five concepts in Azure Event Grid:
    * Events
    * Event sources/publishers
    * Topics
    * Event subscriptions
    * Event handlers
* Event Grid Usage scenarios
    * Serverless application architectures
    * Ops Automation
    * Application integration

### Azure IoT Central[^](https://docs.microsoft.com/en-us/azure/iot-central/overview-iot-central)
* A software as a service (SaaS) offering, to deploy a fully managed, end-to-end solution that enables powerful IoT scenarios without requiring cloud-solution expertise.

### Azure IoT Suite[^](https://docs.microsoft.com/en-us/azure/iot-suite/)
* A platform as a service (PaaS) offering, fully customizable solutions for common scenarios to accelerate your IoT project.

### Azure Relay[^](https://docs.microsoft.com/en-us/azure/service-bus-relay/relay-what-is-it)
* Hybrid connections and WCF Relay are part of Azure Relay service
* Comminicate with on-premises resources without opening a firewall port
* Hybrid connections support multi-platform scenarios
* Hybrid connections can be used to connect to any TCP port including SQL DB's and Web API's 
* WCF Relay can communicate with WCF services and .Net Framework only
* Connect an Azure Web App to on-presmises via VPN
* VNet integration gives a multi tenant Web App Access to resources accessible by an Azure VNet.
* App Service Environment (ASE) can be deployed into an Azure VNet for bidirectional access.

### Useful links
* Compare Queues: [^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-azure-and-service-bus-queues-compared-contrasted)

* Performance:[^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-performance-improvements)

* High-Availability:[^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-async-messaging)

* Premium messaging: [^](https://docs.microsoft.com/en-in/azure/service-bus-messaging/service-bus-premium-messaging)

* Asynchronous Messaging Primer: [^](https://msdn.microsoft.com/library/dn589781.aspx)

* Compare Azure IoT options[^](https://docs.microsoft.com/en-us/azure/iot-suite/iot-suite-options)

* Azure Machine Learning Key Concepts[^](https://docs.microsoft.com/en-in/azure/machine-learning/desktop-workbench/overview-general-concepts)

### Azure Media Services[^](https://docs.microsoft.com/en-in/azure/media-services/media-services-overview)
* Microsoft Azure Media Services is an extensible cloud-based platform that enables developers to build scalable media management and delivery applications
* Azure Media Services concepts[^](https://docs.microsoft.com/en-in/azure/media-services/media-services-concepts)
* Media Services Applications
    * Live event Streaming service with CDN capabilities
    * Studio grade encoding
    * Content protection and encryption
    * Distribute content across multiple channels and devices
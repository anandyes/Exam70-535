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

### Azure Bot Service [^](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction)

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

### Cognitive Services [^](https://azure.microsoft.com/en-us/services/cognitive-services/)
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

# Develop Generative AI Apps in Azure

![Azure AI Overview](https://learn.microsoft.com/en-us/azure/media/ai-services-overview.png)
*Figure: Overview of Azure AI services and platforms*

## Table of Contents
1. [Introduction](#introduction)
2. [Azure AI Services](#azure-ai-services)
3. [Azure AI Foundry](#azure-ai-foundry)
4. [Azure AI Foundry Projects](#azure-ai-foundry-projects)
5. [Responsible AI](#responsible-ai)

## Introduction

The growth in the use of artificial intelligence (AI) in general, and *generative* AI in particular means that developers are increasingly required to create comprehensive AI solutions. These solutions need to combine machine learning models, AI services, prompt engineering solutions, and custom code.

Microsoft Azure provides multiple services that you can use to create AI solutions. However, before embarking on an AI application development project, it's useful to consider the available options for services, tools, and frameworks as well as some principles and practices that can help you succeed.

This module explores some of the key considerations for planning an AI development project, and introduces **Azure AI Foundry**; a comprehensive platform for AI development on Microsoft Azure.

## Azure AI Services

![Azure AI Services Architecture](https://learn.microsoft.com/en-us/azure/media/ai-services-architecture.png)
*Diagram: High-level architecture of Azure AI services*

Microsoft Azure provides a wide range of cloud services that you can use to develop, deploy, and manage an AI solution. The most obvious starting point for considering AI development on Azure is Azure AI services; a set of out-of-the-box prebuilt APIs and models that you can integrate into your applications. The following table lists some commonly used Azure AI services (for a full list of all available Azure AI services, see Available Azure AI services).

| Service | Description |
|---------|-------------|
| **Azure OpenAI** | Azure OpenAI in Foundry Models provides access to OpenAI generative AI models including the GPT family of large and small language models and DALL-E image-generation models within a scalable and securable cloud service on Azure. |
| **Azure AI Vision** | The Azure AI Vision service provides a set of models and APIs that you can use to implement common computer vision functionality in an application. With the AI Vision service, you can detect common objects in images, generate captions, descriptions, and tags based on image contents, and read text in images. |
| **Azure AI Speech** | The Azure AI Speech service provides APIs that you can use to implement *text to speech* and *speech to text* transformation, as well as specialized speech-based capabilities like speaker recognition and translation. |
| **Azure AI Language** | The Azure AI Language service provides models and APIs that you can use to analyze natural language text and perform tasks such as entity extraction, sentiment analysis, and summarization. The AI Language service also provides functionality to help you build conversational language models and question answering solutions. |
| **Azure AI Foundry Content Safety** | Azure AI Foundry Content Safety provides developers with access to advanced algorithms for processing images and text and flagging content that is potentially offensive, risky, or otherwise undesirable. |
| **Azure AI Translator** | The Azure AI Translator service uses state-of-the-art language models to translate text between a large number of languages. |
| **Azure AI Face** | The Azure AI Face service is a specialist computer vision implementation that can detect, analyze, and recognize human faces. Because of the potential risks associated with personal identification and misuse of this capability, access to some features of the AI Face service are restricted to approved customers. |
| **Azure AI Custom Vision** | The Azure AI Custom Vision service enables you to train and use custom computer vision models for image classification and object detection. |
| **Azure AI Document Intelligence** | With Azure AI Document Intelligence, you can use pre-built or custom models to extract fields from complex documents such as invoices, receipts, and forms. |
| **Azure AI Content Understanding** | The Azure AI Content Understanding service provides multi-modal content analysis capabilities that enable you to build models to extract data from forms and documents, images, videos, and audio streams. |
| **Azure AI Search** | The Azure AI Search service uses a pipeline of AI skills based on other Azure AI Services and custom code to extract information from content and create a searchable index. AI Search is commonly used to create vector indexes for data that can then be used to *ground* prompts submitted to generative AI language models, such as those provided in Azure OpenAI. |

## Azure AI Foundry

Azure AI Foundry is a platform for AI development on Microsoft Azure. While you *can* provision individual Azure AI services resources and build applications that consume them without it, the project organization, resource management, and AI development capabilities of Azure AI Foundry makes it the recommended way to build all but the most simple solutions.

Azure AI Foundry provides the *Azure AI Foundry portal*, a web-based visual interface for working with AI projects. It also provides the *Azure AI Foundry SDK*, which you can use to build AI solutions programmatically.

![Azure AI Foundry Platform Diagram](https://learn.microsoft.com/en-us/azure/media/ai-foundry-platform-diagram.png)
*Diagram: Azure AI Foundry platform components*

### Key Features of Azure AI Foundry

![Azure AI Foundry Portal Features](https://learn.microsoft.com/en-us/azure/media/ai-foundry-portal-features.png)
*Diagram: Features of the Azure AI Foundry portal*

**Azure AI Foundry Portal**
The Azure AI Foundry portal provides a comprehensive web-based interface for managing AI projects, deploying models, and building AI applications. The portal includes:
- Project management and collaboration tools
- Model deployment and testing capabilities
- Built-in playgrounds for experimenting with AI models
- Resource management and monitoring tools

**Azure AI Foundry SDK**
The SDK enables programmatic access to Azure AI Foundry capabilities, allowing developers to:
- Build AI solutions using code
- Integrate AI capabilities into existing applications
- Automate deployment and management processes
- Create custom AI workflows and pipelines

## Azure AI Foundry Projects

![Foundry vs Hub-based Projects Diagram](https://learn.microsoft.com/en-us/azure/media/foundry-vs-hub-diagram.png)
*Diagram: Comparison of Foundry and Hub-based project structures*

In Azure AI Foundry, you manage the resource connections, data, code, and other elements of the AI solution in *projects*. There are two kinds of project:

### Foundry Projects

*Foundry projects* are associated with an **Azure AI Foundry** resource in an Azure subscription. Foundry projects provide support for Azure AI Foundry models (including OpenAI models), Azure AI Foundry Agent Service, Azure AI services, and tools for evaluation and responsible AI development.

An Azure AI Foundry resource supports the most common AI development tasks to develop generative AI chat apps and agents. In most cases, using a Foundry project provides the right level of resource centralization and capabilities with a minimal amount of administrative resource management. You can use Azure AI Foundry portal to work in projects that are based in Azure AI Foundry resources, making it easy to add connected resources and manage model and agent deployments.

**Key Features of Foundry Projects:**
- Access to Azure OpenAI models and other AI Foundry models
- Integration with Azure AI Foundry Agent Service
- Built-in evaluation and responsible AI tools
- Simplified resource management
- Streamlined deployment processes

### Hub-based Projects

*Hub-based projects* are associated with an **Azure AI hub** resource in an Azure subscription. Hub-based projects include an Azure AI Foundry resource, as well as managed compute, support for Prompt Flow development, and connected **Azure storage** and **Azure key vault** resources for secure data storage.

Azure AI hub resources support advanced AI development scenarios, like developing Prompt Flow based applications or fine-tuning models. You can also use Azure AI hub resources in both Azure AI Foundry portal and Azure Machine learning portal, making it easier to work on collaborative projects that involve data scientists and machine learning specialists as well as developers and AI software engineers.

**Key Features of Hub-based Projects:**
- Advanced AI development capabilities
- Prompt Flow development support
- Model fine-tuning capabilities
- Managed compute resources
- Secure data storage with Azure Storage and Key Vault
- Integration with Azure Machine Learning
- Support for collaborative development teams

### Choosing the Right Project Type

**Choose Foundry Projects when:**
- Building generative AI chat applications or agents
- Working on straightforward AI development tasks
- Preferring minimal administrative overhead
- Focusing on Azure OpenAI models and standard AI services

**Choose Hub-based Projects when:**
- Developing complex AI solutions requiring custom workflows
- Need for Prompt Flow development
- Requiring model fine-tuning capabilities
- Working with collaborative teams including data scientists
- Need advanced compute and storage management
- Building enterprise-grade AI applications with enhanced security

## Responsible AI

![Responsible AI Principles Diagram](https://learn.microsoft.com/en-us/azure/media/responsible-ai-diagram.png)
*Diagram: Microsoft Responsible AI principles*

It's important for software engineers to consider the impact of their software on users, and society in general; including considerations for its responsible use. When the application is imbued with artificial intelligence, these considerations are particularly important due to the nature of how AI systems work and inform decisions; often based on probabilistic models, which are in turn dependent on the data with which they were trained.

The human-like nature of AI solutions is a significant benefit in making applications user-friendly, but it can also lead users to place a great deal of trust in the application's ability to make correct decisions. The potential for harm to individuals or groups through incorrect predictions or misuse of AI capabilities is a major concern, and software engineers building AI-enabled solutions should apply due consideration to mitigate risks and ensure fairness, reliability, and adequate protection from harm or discrimination.

Let's discuss some core principles for responsible AI that have been adopted at Microsoft.

### Fairness

AI systems should treat all people fairly. For example, suppose you create a machine learning model to support a loan approval application for a bank. The model should make predictions of whether or not the loan should be approved without incorporating any bias based on gender, ethnicity, or other factors that might result in an unfair advantage or disadvantage to specific groups of applicants.

Fairness of machine learned systems is a highly active area of ongoing research, and some software solutions exist for evaluating, quantifying, and mitigating unfairness in machine learned models. However, tooling alone isn't sufficient to ensure fairness. Consider fairness from the beginning of the application development process; carefully reviewing training data to ensure it's representative of all potentially affected subjects, and evaluating predictive performance for subsections of your user population throughout the development lifecycle.

### Reliability and Safety

AI systems should perform reliably and safely. For example, consider an AI-based software system for an autonomous vehicle; or a machine learning model that diagnoses patient symptoms and recommends prescriptions. Unreliability in these kinds of system can result in substantial risk to human life.

As with any software, AI-based software application development must be subjected to rigorous testing and deployment management processes to ensure that they work as expected before release. Additionally, software engineers need to take into account the probabilistic nature of machine learning models, and apply appropriate thresholds when evaluating confidence scores for predictions.

### Privacy and Security

AI systems should be secure and respect privacy. The machine learning models on which AI systems are based rely on large volumes of data, which may contain personal details that must be kept private. Even after models are trained and the system is in production, they use new data to make predictions or take action that may be subject to privacy or security concerns; so appropriate safeguards to protect data and customer content must be implemented.

### Inclusiveness

AI systems should empower everyone and engage people. AI should bring benefits to all parts of society, regardless of physical ability, gender, sexual orientation, ethnicity, or other factors.

One way to optimize for inclusiveness is to ensure that the design, development, and testing of your application includes input from as diverse a group of people as possible.

### Transparency

AI systems should be understandable. Users should be made fully aware of the purpose of the system, how it works, and what limitations may be expected.

For example, when an AI system is based on a machine learning model, you should generally make users aware of factors that may affect the accuracy of its predictions, such as the number of cases used to train the model, or the specific features that have the most influence over its predictions. You should also share information about the confidence score for predictions.

When an AI application relies on personal data, such as a facial recognition system that takes images of people to recognize them; you should make it clear to the user how their data is used and retained, and who has access to it.

### Accountability

People should be accountable for AI systems. Although many AI systems seem to operate autonomously, ultimately it's the responsibility of the developers who trained and validated the models they use, and defined the logic that bases decisions on model predictions to ensure that the overall system meets responsibility requirements. To help meet this goal, designers and developers of AI-based solution should work within a framework of governance and organizational principles that ensure the solution meets responsible and legal standards that are clearly defined.

## Getting Started with Azure AI Foundry

![Azure AI Foundry Workflow](https://learn.microsoft.com/en-us/azure/media/ai-foundry-workflow.png)
*Diagram: Typical workflow for building AI solutions in Azure AI Foundry*

To begin your AI development journey with Azure AI Foundry:

1. **Access the Portal**: Navigate to the Azure AI Foundry portal at https://ai.azure.com
2. **Create a Project**: Choose between Foundry or Hub-based projects based on your requirements
3. **Select Models**: Browse and deploy the AI models that best fit your use case
4. **Configure Resources**: Set up the necessary Azure resources and connections
5. **Start Building**: Use the playground to test models and begin developing your AI solution

Azure AI Foundry provides the comprehensive platform and tools needed to build responsible, scalable, and effective AI applications on Microsoft Azure.

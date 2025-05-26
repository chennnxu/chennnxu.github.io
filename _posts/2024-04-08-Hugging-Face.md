---
layout: post
title: Hugging Face & MLflow & LLMOps
# subtitle: MLflow
cover-img: /assets/img/hf-logo-with-title.png
tags: [ML, MLOps]
comments: true
---
<!-- this is the notes for Coursera MlOps of Duke University -->
# HuggingFace

## 0. Key Terms

**Model Hub** - Repository of thousands of reusable trained ML models
**Spaces** - Hosted apps to demonstrate ML projects  
**Codespaces** - Browser-based dev environment with GPU access
**CLI** - Command line tool for tasks like authentication and caching  
**Inference API** - Hosted API to get predictions from latest models  

## 1. Reflections

1. What benefits does the HuggingFace Hub provide over sharing models on GitHub or personal websites?  
2. What ethical concerns might arise from the open sharing of machine learning models? How might HuggingFace aim to address them?  
3. What are some key differences between the services and content provided by HuggingFace versus other AI providers?  
4. How feasible would it be for an individual researcher or small team to share their work on HuggingFace? What might be difficult?  
5. Could the HuggingFace Hub reduce duplication of effort in the machine learning research community? In what ways?  

# MLflow

## 0. Key Terms

**MLflow Tracking** - Logs key metrics, parameters, models, and other artifacts when running ML code to monitor experiments  
**MLflow Projects** - Configurable standard format for organizing ML code to ensure consistency and reproducibility  
**MLflow Models** - Package ML model files with their dependencies so they can be deployed on diverse platforms  
**Entry Points** - Define the scripts that can be executed within the project workflow  
**Conda Environment** - Specifies the dependencies and software required to recreate the runtime environment  
**Model Registry** – Centralized model storage to manage versions and lifecycle  
**MLflow Artifacts** – Files including model, Conda YAML that detail software environment  
**MLflow Serve** – Expose packaged model via real-time inference REST API

## 1. Install & Use MLflow

Install MLflow

```python
pip3 install mlflow
```

Interact with MLflow UI

```python
mlflow ui
```

Executes an MLflow project locally or from a Git repo with given parameters

```python
mlflow run
```

## 2. Reflections

### MLflow

- How could MLflow improve collaboration in a machine learning team?
- What components of MLflow seem most useful for managing machine learning experiments?
- How might MLflow help address reproducibility issues in machine learning?
- What kinds of challenges could arise when scaling up MLflow to large datasets or models?

### MLflow Projects

- How do MLflow Projects differ from simply version controlling and sharing code? What additional value do they provide?
- What kinds of challenges could arise when trying to break up a machine learning pipeline into separate reusable steps? How might MLflow help address some of these?
- What are some examples of workflows or use cases that would benefit from being implemented as MLflow Projects?
- How feasible would it be to convert an existing machine learning codebase into an MLflow Project? What would be involved?

### MLflow Models

- What are some advantages of the different deployment options offered by MLflow? When might you choose one over the other?
- How does MLflow make deployment more portable across different platforms? What challenges might still arise?
- Why is the python_function flavor important for deployment? What are some limitations?
- How feasible would it be to take a model deployed locally and migrate it to SageMaker? What would need to change?
- Could the MLflow Model format replace the need for ONNX or PMML model formats? Why or why not?

## 3. Rescources

[MLflow document](https://mlflow.org/docs/latest/introduction/index.html)  
[MLflow Projects](https://mlflow.org/docs/latest/projects.html)  
[MLflow Models](https://mlflow.org/docs/latest/models.html)

## LLMOps Key Terms

**Tokenizer** - The process of splitting text into smaller chunks or "tokens" and assigning each one a number.  
**Encoding** - Converting the text tokens into numeric representations.  
**Probability machine** - How LLMs work by predicting the probability of the next token based on the previous ones.  
**Fine-tuning** - Further training a pretrained LLM on more specific data to adapt it to a particular task.  
**Prompt engineering** - Crafting the input text carefully to get better results from an LLM.  
**Retrieval augmentation** - Combining search/retrieval with an LLM to improve results.  
**Risk mitigation** - Strategies like prompt engineering and fine-tuning to reduce risks of using LLMs.  
**Foundation model** - A large pretrained deep learning model that can be adapted to other tasks.  
**Repurposing** - Using a foundation model for a task different than its original purpose.  
**Code assistant** - An example application built by fine-tuning a foundation model for coding.  
**Azure OpenAI Service** - Allows using OpenAI models like GPT-3 on the Microsoft Azure cloud.  
**Inference API** - Using a trained model to generate predictions/outputs from new data.  
**Local model** - Running an AI model like GPT-3 directly on your own computer.  
**LAMA-file** - A project from Mozilla to easily run models locally.  
**Interactive API** - Calling the cloud service API to get outputs from the deployed model.  
**Prompt engineering** - The practice of carefully crafting prompts to provide context and get better responses from AI systems.  
**Context** - Additional background information provided in a prompt to help the AI understand and provide a more relevant response.  
**Zero shot prompting** - Providing an instruction without any examples to generate a response.  
**One shot prompting** - Providing one example along with an instruction to guide the AI's response.  
**Few shot prompting** - Providing two or more examples along with an instruction to guide the AI's response.  
**Interface** - The means of interacting with the AI system, like a chat or text box.  
**Context overload** - Providing too much context and instructions can overwhelm the AI, resulting in poor or incomplete responses.  
**Chain of thought** - Prompting the AI to explain its reasoning step-by-step. Useful for getting more detailed responses.  
**Rephrasing** - Restating or rewording a prompt to get better results from the AI. Helps clarify intent.  
**API-based application**: An application that interacts with other software components using Application Programming Interfaces (APIs) for data exchange, communication, or functionality enhancement.[Example](https://github.com/alfredodeza/azure-chat-demo)  
**Embedded model application**: A machine learning model integrated within an application, allowing the app to perform specific tasks without relying on external services.[Example](https://github.com/alfredodeza/huggingface-deploy-azure.git)  
**Multi-model application**: An AI system that utilizes multiple models tailored to different functions or domains, improving efficiency and performance in various scenarios.  
**HTTP API**: An interface for exchanging data between systems using Hypertext Transfer Protocol (HTTP) requests and responses over the internet.  
**Azure OpenAI**: A cloud-based platform by Microsoft that offers access to large language models through an easy-to-use API, enabling developers to build AI applications with advanced text generation capabilities.  
**Separation of concerns**: A design principle that suggests dividing complex systems into smaller, independent components responsible for specific functions, improving maintainability and scalability.  
**Scale/Scalability**: The ability of an application or system to handle increasing workloads efficiently by adding resources (e.g., computing power, storage) without significantly impacting performance or functionality.  
**Retrieval augmented generation (RAG)**: A technique in AI where a large language model accesses new or recent data outside its training set to provide better answers and improved results.[Example](https://github.com/alfredodeza/azure-rag.git)  

### Open Source LLMOps Solutions

**Model license**- The license terms that determine how a machine learning model can be used, modified and shared. Common open source licenses for models include Apache, MIT and Creative Commons. The license affects what you can do commercially with a model.  
**Large language model** - A neural network trained on massive amounts of text data to generate human-like text. Large language models have billions of parameters and are able to perform a variety of natural language tasks like translation, summarization, and question answering.  
**Small language model** - A large language model with fewer parameters, requiring less compute resources than larger models. Smaller models can be more practical to deploy but may be less capable.  
**Transformers library** - An open source Python library from Hugging Face for leveraging machine learning models, particularly natural language models. Provides a simple, unified API for using models from different frameworks like PyTorch and TensorFlow.  

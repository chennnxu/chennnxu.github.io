---
layout: post
title: Hugging Face & MLflow
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

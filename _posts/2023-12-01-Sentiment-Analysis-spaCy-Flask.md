---
layout: post
title: Sentiment Analysis Application with spaCy and Flask
thumbnail-img: /assets/img/sentiment_analysis.png
tags: [Project, Full Stack, NLP]
---
## Highlight
```
spaCy, Flask, unit test, static code analysis
```

## Overview

In this project, we make use of the spaCy, to create an application that would perform sentiment analysis on a provided text. We then deploy this application over the web using Flask framework.

## Main Steps

<div align = "center">
<img src="../assets/img/sentimentAnalysisWorkflow.png" width = "300" alt="saw" align=center />
<p class="text-center">Figure 1 Main Steps</p>
</div>

The main steps for completing this project are shown in Figure 1. And the running code can be found in [GitHub](https://github.com/chennnxu/Project_Sentiment-Analysis-Application-with-Flask.git).

* Step 1 & 2: Create a sentiment analysis application & Package the application
  
> Create a folder `SentimentAnalysis` (aka **Package**).
  Create two files `__init__.py` and `sentiment_analysis.py` (aka **module**) in the folder, define `sentiment_analysis_func` in `sentiment_analysis.py` file.

* Step 3: Run unit tests on the application

> 
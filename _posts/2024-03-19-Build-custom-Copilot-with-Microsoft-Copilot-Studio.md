---
layout: post
title: Build custom Copilot with Microsoft Copilot Studio
tags: [Project, Copilot]
---

## Highlight

```text
Custom Copilot, Generative Answers, Generative Actions
```

<!-- 这次活动是Microsoft AI Tour，那么主题肯定是宣传Microsoft自家的AI产品。根据自己以往参加活动的经验，大部分session talks太过于高屋建瓴了且时长有限，对于自己来说门槛较高，也就是说很多时候听的似懂非懂。所以我对workshop更感兴趣，毕竟可以动手写代码或是动手做个项目，总能够学习些东西。 -->

# Overview

## What is Microsoft Copilot Studio?

Microsoft Copilot Studio, which provide the fastest way to build Generative AI Copilot.

<!-- 那么对我来, 目标是了解Copilot Studio并且能够开发自己的Copilot Studio，是件非常酷的事情。 -->

<!-- Workshop is well-structured. We are first introduced what we are going to do and some main concepts and then finish the project ourselves by following the instruction. -->

## Build Custom Copilot called "Pandora"

Following I will build my own Copilot - "Pandora", with Generative Answers and Generative Actions.

### Generative Answers

My understanding of generative answers is that they enable you to use Copilot to talk with your own data.

#### Build the Copilot

* Press Create Copilot and give it a name.
* Give knowledge source, e.g. a website, to the Copilot for genrative answers, so that the copilot can instantly answer the question over the data.
* Test the copilot! Yes, It's surprisingly easy to get started with Copilot, just a few steps and you're good to go.

#### Publish the Copilot

* Press Publish to publish the copilot, so that the copilot can be added to other channels, e.g. Microsoft Teams, WhatsApp, twilio, Facebook etc.
* Select the channel, e.g. Microsoft Teams.
* Open Bot and then will be redirected to Microsoft Teams
* Add the Copilot to Teams. Now we can use the Copilot on Teams.

### Generative Actions

#### Build a plugin/custom connetor

Build a plugin/custom connetor for the Copilot so that the Copilot can work with other systems expanding its capabilities beyond answering questions. For example work with APIs to look up certain information or update certain information.

#### Add the connector to Microsoft Copilot Studio

Add the connector to Microsoft Copilot Studio "Connected Services > Add > Microsoft Power Platform > Sign in Microsoft Power Platform > Fill in some information"

#### Add the Plugin to custom Copilot "Pandora"

* Press Create Plugin/Action and search the Plugin we added.
* Run the application and test the custom Copilot.

### What is the differece between ChatGPT and Microsoft Copilot?

* Similarity
  * both are AI tools
  * both work like a chatbot

* Difference
  * GPT in ChatGPT stands for “generative pre-trained transformer”. After giving it a question or prompt, ChatGPT understands the context of the conversation and generate the appropriate responses.
  * Microsoft Copilot is an AI-powered digital assistant that aims to provide personalized assistance to users for a range of tasks and activities.

## Reference

Microsoft AI Tour Berlin 03.19.2024  
Workshop 1: Build your own Copilot with Microsoft Copilot Studio  
[ChatGPT vs. Microsoft Copilot: What's the difference?](https://support.microsoft.com/en-us/topic/chatgpt-vs-microsoft-copilot-what-s-the-difference-8fdec864-72b1-46e1-afcb-8c12280d712f)

## Learn more

* [Copilot Studio website](https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio)  
* [Blog](https://www.microsoft.com/en-us/microsoft-365/blog/2023/11/15/announcing-microsoft-copilot-studio-customize-copilot-for-microsoft-365-and-build-your-own-standalone-copilots/)  
* [Demo](https://web.powerva.microsoft.com/tryit)  
* [Sizzle video](https://www.youtube.com/watch?v=WVn57PXoFPE)  
* [Product Document](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)  
* [Community Page](https://powerusers.microsoft.com/t5/Copilot-Studio-Community/ct-p/PVACommunity)  
* [Implementation Studio](https://www.bing.com/?ref=aka&shorturl=CopilotStudioImplenmentationGuide)

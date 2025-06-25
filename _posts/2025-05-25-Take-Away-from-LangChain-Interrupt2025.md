---
layout: post
title: Take Away from LangChain Interrupt 2025
subtitle: THE AI AGENT CONFERENCE BY LANGCHAIN
cover-img: /assets/img/langchain_interrupt_2025/langchain_interrupt_2025.png
thumbnail-img: /assets/img/langchain_interrupt_2025/langchain_interrupt_2025.png
# share-img: /assets/img/path.jpg
tags: [LangChain, AI Agent]
---

LLMs are amazing and super powerful. They can transform the types of applications that we can build. And there's a lot of tooling that needs to be built around them to really help us take advantage of all their capabilities.

### 🤖️The ingredients of building agents

- Prompting
- Engineering
- Product(Product sense & Product skills)
- Machine learning

<div align = "center">
<img src="/assets/img/langchain_interrupt_2025/ingredients.png" width = "800" alt="ingredients" align=center />
</div>

Being good at ***Prompting*** is a core component of building agents. And ***Engineering*** is also a core component. There is a lot of engineering skills that go into building reliable agents. Whether it's the tools that they're using and interacting with, whether it's the patterns that we're using to to do the data pipelines that bring the context to the LLM at the right point of time, whether it's the deployment, there's a lot of engineering that goes into building agents. There's a lot of ***Product sense and Product skills*** as well. This is similar to the product engineer before, but now when we're building agents, we're often building them to do workflows that a human or a group of humans would do. And so having the product sense and intuition and skill to understand those flows and then try to replicate them with an agent is a really important skill. And finally, there's some aspects of ***Machine Learning*** that are involved. So most prominently with evals, we see this being a great way to test and and measure these agents and capture the the non-determinism with some metrics over time. And there's other things like fine-tuning as well. And the combination of all of these skills has really burged into what we see being the ***Agent Engineer***. LangChain exists to support the agent engineer.

### 💡What will the agents of the future look like?

Look what agents like and so then LangChain build tools to help build those agents. There are a few beliefs that they have. Three of them are more kind of like in the present/now and three of them which are in the future.

#### Belief #1: Agents rely on many different models

Over the past year, there have been a lot of different models coming on to the playing field. They have different strengths and weaknesses. Some of them are really costly but they can reason for a long time. Some of them are faster and they're better for specific tasks. Some of them are great at reasoning. Some of them are great at writing. And so this whole ecosystem of models out there giving developers the choice to choose which model is best for them at a particular point in their agent. So an agent might use many different models and we see that being an increasingly common thing. [Check Models Here](https://www.datalearner.com/ai-models/ai-benchmarks-tests/benchmarks-for-all).
This is where the original LangChain package turned into. A big part of that was the *integrations*, a place for integrations of all types but specifically for language models as we've seen this be the key component of building these applications and it's provided a a stable ecosystem for interacting with all the different model providers.

<div align = "center">
<img src="/assets/img/langchain_interrupt_2025/ecosystem.png" width = "800" alt="ecosystem" align=center />
</div>

#### Belief #2: Reliable Agents start with the right context

So prompting is really important. The prompt that you construct to pass into the LLM will determine what comes out of the LLM that will determine the behavior of the agent. This prompt isn't just one big string. It's actually made up of a bunch of different parts. And all these parts come from different places. So they could come from a system message. They could come from user input. They could come from tools. They could come from retrieval steps. They could come from the conversation history. And so when you construct this context that you're passing into the LLM, it's really really important to be able to control exactly what goes in there because that will affect what comes out.

And so in order to provide this control and flexibility in this context engineering, They've started moving all of agent orchestration over to ***LangGraph***. You can create the flow of the agent that you want. So, you can do all the necessary steps to get the right context and then you can pass that in whatever form to the LLM. And so, you have supreme control over all of it. And this controllability to build the cognitive architecture that you want is a key selling point of LangGraph as the ***agent orchestration framework***.

Full control over the cognitive architecture of your application, so you can get the right context.

- streaming
- human in the loop
- short-term memory
- long-term memory
- durable execution

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/context.png" width="800" alt="context" align=center />
</div>

#### Belief #3: Building agents is a team sport

We think there are all these different areas (prompting, engineeer, product, machine learning) that are involved in building agents. Ideally one person, the agent engineer, would have all of these assets, but it's early on. We're still figuring out what these means. And so building agents is becoming a team sport. *LangSmith* helps. The observability, evaluability that it provides as a really integral way for everyone, but especially *product* people to see what's going on inside the agent. So you can see all the steps that are happening, you can see the inputs and outputs. And so if you're trying to replicate a human workflow that you understand, this provides the best kind of like pane of glass into what's happening. 

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langsmith_tracing.png" width="800" alt="langsmith_tracing" align=center />
</div>

Eval being important, this is where the *machine learning* knowledge comes into play. It incredibly easy to build data sets and run evals both offline and online in LangSmith. 

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langsmith_ml.png" width="800" alt="langsmith_ml" align=center />
</div>

And finally, *prompting*. Prompting is a key part of building agents. There is a prompt hub and prompt playground. The reason that all of these are in the same platform, LangSmith, is because agent building is a team sport and there needs to be this platform for all these people of different backgrounds and strengths to collaborate on agents in one place.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langsmith_prompting.png" width="800" alt="langsmith_prompting" align=center />
</div>

So these are three beliefs about what it's like to build agents now.

### 😄Where do we think the industry is headed?

#### Belief #4: AI observability is different

As we see more and more agents going into production, one of the things that we're starting to believe more strongly is that AI observability is different than traditional observability. When you're dealing with agents, you're getting all of these *large, unstructured often multimodal payloads* that are coming into a platform. And those are some technical differences from traditional observability. But also what's different is the user persona that the observability logs are being used for. They're not built for an SRE. They're *built for agent engineer* persona. And that needs to bring in some of these ML concepts, some of that product concepts, some of that prompt engineering context and provide this different type of AI observability. And we've always had AI observability in LangSmith from traditional metrics to business metrics to more qualitative metrics. And metrics around agents. So you can track the run counts of tools, the latencies, the errors. And then also trajectory observability so you can see which paths your agents are taking and again the latency and errors associated with that. And so this AI Oberservability available in Langmith.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langsmith_observability.png" width="800" alt="langsmith_observability" align=center />
</div>

#### Belief #5: Everyone will be an agent builder

When we talk about this agent engineer, it combines four different aspects. And realistically right now it's so early on that no one really is at the center of all this and has all of these skills. To make it possible for people to collaborate and build agents as a team sport. and this is LangSmith. But to folks who are maybe in one of these quadrants, in a traditional engineering background or or in a product background or in an ML background, move them more towards the center so that they can build agents.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/3_levels.png" width="800" alt="3_levels" align=center />
</div>

So if we think about developers who don't have a background in AI and aren't familiar with this, how can we enable them to build agents more easily? *Langraph Prebuilts*. So these are common agent architectures for the variety of different agent types that we see out there. So single agents, agent swarms, supervisor agents, there's some other ones as well. It makes really easy for anyone who doesn't understand agents or is coming to it from an engineering background to easily get started with these common architectures.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langgraph_prebuilts.png" width="800" alt="langgraph_prebuilts" align=center />
</div>

At the next level, for people who are on these product engineering teams but maybe not developers themselves to be more involved in building agents. So, one of the coolest things is *LangGraph Studio*. 

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langgraph_studio.png" width="800" alt="langgraph_studio" align=center />
</div>

And then finally if we want to make it possible for people who aren't developers at all to build agents from scratch, to build agents in a no code way. *Open Agent platform*. It's powered by LangGraph platform. It uses agent templates to allow people to build agents in a no code way. It comes with a tool server that uses MCP. It comes with RAG as a service so you can easily get started with anything related to RAG and it contains an agent registry so that you can see all the different agents that you've created.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/open_agent_platform.png" width="800" alt="open_agent_platform" align=center />
</div>

#### Belief #6: Deployment of the Agents is the next hurdle

Once we build an agent, then need to deploy it. And sometimes this can be easy, like a traditional web server and put it behind it. But we see more and more that agents are looking a little bit different than traditional web apps. Specifically, they're often *long running*.They're often *bursty* in nature, and they're *flaky*. They're flaky in a bunch of different ways. The calls to the LLM might fail, also you want to have human in the loop because these LLMs might not do what you expect. And you need some statefulness in these agents to allow this human in the loop or human on the loop interaction patterns. *Langraph Platform*. It scales horizontally so it can handle burstiness. It's designed for these long running workloads and you can actually expose the agents that you deploy here as MCP servers. It also comes with a control plane where you can discover the agents that everyone at your or has deployed. You can share agents. You can reuse these agents with templates. And then there are a few different deployment options, cloud SAS offering as well as hybrid and then fully self-hosted options.

<div align="center">
<img src="/assets/img/langchain_interrupt_2025/langgraph_platform.png" width="800" alt="langgraph_platform" align=center />
</div>

### 🤔Summary

- LangChain 多模型glue层
- LangGraph 智能体orchestrator
- LangSmith 团队协作+AI observation
- LangGraph Prebuilts 面向传统Engineer
- LangGraph Studio 面向产品Engineer
- Open Agent Platform 低代码 for everyone
- LangGraph Platform 部署和服务化

## Resources

- [LangChain Interrupt 2025](https://interrupt.langchain.com)
- [Interrupt 2025 Keynote - Harrison Chase (LangChain) - YouTube](https://www.youtube.com/watch?v=DrygcOI-kG8)

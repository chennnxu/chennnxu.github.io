---
layout: post
title: Take Away from LangChain Interrupt 2025
# subtitle: Black Myth
cover-img: /assets/img/langchain_interrupt_2025/langchain_interrupt_2025.png
thumbnail-img: /assets/img/langchain_interrupt_2025/langchain_interrupt_2025.png
# share-img: /assets/img/path.jpg
tags: [LangChain, Agent]
---

> LLMs are amazing and super powerful. They can transform the types of applications that we can build. And there's a lot of tooling that needs to be built around them to really help us take advantage of all their capabilities.

### 🤖️The ingredients of building agents

- Prompting
- Engineering
- Product(Product sense & Product skills)
- Machine learning

<div align = "center">
<img src="/assets/img/langchain_interrupt_2025/ingredients.png" width = "400" alt="ingredients" align=center />
</div>

Being good at ***Prompting*** is a core component of building agents. And ***Engineering*** is also a core component. There is a lot of engineering skills that go into building reliable agents. Whether it's the tools that they're using and interacting with, whether it's the patterns that they're using to to do the data pipelines that bring the context to the LLM at the right point of time, whether it's the deployment, there's a lot of engineering that goes into building agents. There's a lot of ***Product sense and Product skills*** as well. This is similar to the product engineer before, but now when we're building agents, we're often building them to do workflows that a human or a group of humans would do. And so having the product sense and intuition and skill to understand those flows and then try to replicate them with an agent is a really important skill. And finally, there's some aspects of ***Machine Learning*** that are involved. So most prominently with evals, we see this being a great way to test and and measure these agents and capture the the non-determinism with some metrics over time. And there's other things like fine-tuning as well. And the combination of all of these skills has really burged into what we see being the ***Agent Engineer***. LangChain exists to support the agent engineer.

### 💡What will the agents of the future look like?

Look what agents like and so then LangChain build tools to help build those agents. There are a few beliefs that they have. Three of them are more kind of like in the present/now and three of them which are in the future.

#### Belief #1: Agents rely on many different models

Over the past year, there have been a lot of different models coming on to the playing field. They have different strengths and weaknesses. Some of them are really costly but they can reason for a long time. Some of them are faster and they're better for specific tasks. Some of them are great at reasoning. Some of them are great at writing. And so this whole ecosystem of models out there giving developers the choice to choose which model is best for them at a particular point in their agent. So an agent might use many different models and we see that being an increasingly common thing.
This is where the original LangChain package turned into. A big part of that was the *integrations*, a place for integrations of all types but specifically for language models as we've seen this be the key component of building these applications and it's provided a a stable ecosystem for interacting with all the different model providers.

<div align = "center">
<img src="/assets/img/langchain_interrupt_2025/ecosystem.png" width = "400" alt="ingredients" align=center />
</div>

#### Belief #2: Reliable Agents start with the right context

The second belief that we have is that reliable agents start with the right context. So what does this mean? So prompting is really important. The prompt that you construct to pass into the LLM will determine what comes out of the LM that will determine the behavior of the agent. This prompt isn't just one big string.

It's actually made up of a bunch of different parts. And all these parts come from different places. So they could come from a system message. They could come from user input. They could come from tools. They could come from retrieval steps. They could come from the the conversation history. And so when you construct this context that you're passing into the LLM, it's really really important to be able to control exactly what goes in there because that will affect what comes out.

And so in order to provide this control and flexibility in this in this context engineering, we've started moving all of our agent orchestration over to *Langraph*. So we launched Langraph a little over a year ago. It's an extremely low-level unopinionated framework for building agents. There's no hidden prompts. There's no hidden cognitive architectures.

You can create the the the the flow of the agent that you want. So, you can do all the necessary steps to get the right context and then you can pass that in whatever form to the LLM. And so, you have supreme control over kind of like all of it. And this this controllability to build the cognitive architecture that you want is a key selling point of of of of langraph as the *agent orchestration framework*.

*Full control over the cognitive architecture of your application, so you can get the right context.*

nd of course on top of this control we've tried to add in functionality that doesn't get in the way of adding the right context.

- 1.streaming
- 2.human in the loop
- 3.short-term memory
- 4.long-term memory
- 5.durable execution

#### Belief #3: Building agents is a team sport

But we think there are all these different areas prompting product machine learning that are involved in building agents. And yes, ideally one person, the agent engineer, would have all of these assets, but it's early on. We're still figuring out what these means.
And so building agents is becoming a team sport. And the way that we're helping with that or trying to help with that is *LangSmith*. So Lang Smith, we think of observability, evaluability that it provides as a really integral way for everyone, but especially *product* people to see what's going on inside the agent. So you can see all the steps that are happening, you can see the inputs and outputs. And so if you're trying to replicate a human workflow that you understand, this provides the best kind of like pane of glass into what's happening. I mentioned eval being important, this is where the *machine learning* knowledge comes into play. And so we try to make it incredibly easy to build data sets and run evals both offline and online in Langmith and provide that team functionality there. And finally, *prompting*. Prompting is a key part of building agents. We have a prompt hub. We have a prompt playground. The reason that all of these are in the same platform, Langmith, is because we think agent building agents is a team sport and there needs to be this platform for all these people of different backgrounds and strengths to collaborate on agents in one place.

So those are three beliefs that we've built up over the past few years about what it's like to build agents now.

### Where do we think the industry is headed?

#### Belief #4: AI observability is different

What are some beliefs we have about the future? As we see more and more agents going into production, one of the things that we're starting to believe more strongly is that AI observability is different than tra than traditional observability.

So what I mean by that is when you're dealing with agents, you're getting all of these *large unstructured often multimodal payloads* that are coming in to a platform. And those are some technical differences from traditional observability. But also what's different is the user persona that the observability logs are being used for. They're not built for an SRE. They're *built for this agent engineer* persona. And that needs to bring in some of these ML concepts, some of that product concepts, some of that prompt engineering context and provide this different type of AI observability. And we've always had AI observability in Langmith from traditional metrics to business metrics to more qualitative metrics.

And today we're excited to launch a new series of metrics around agents. So specifically, we're launching better insight into the tools that your agents are using. So you can track the run counts of tools, the latencies, the errors. And then we're also launching trajectory observability so you can see which paths your agents are taking and again the latency and errors associated with that. And so this AI Oberservability available today in Langmith. If you go and send a bunch of traces, you can start to see this populate. 

#### Belief #5: Everyone will be an agent builder

The next belief we have is that everyone will build be an agent builder. So when we talk about this agent engineer, it it combines these four different aspects. And realistically right now it's so early on that no one really is at the center of all this and and has all of these skills.

And so yes, we want to make it possible for people to collaborate and build agents as a team sport. and this is Linkmith. But we also want to try to move folks who are maybe in one of these quadrants in a traditional engineering background or or in a product background or in an ML background, move them more towards the center so that they can build agents.

So what does that mean? So if if we think about developers who don't have a background in AI and aren't familiar with this, how can we enable them to build agents more easily? The thing that we've been building towards this, we've launched a few things over the past few months in this is what we're calling *Langraph Prebuilts*.

So these are common agent architectures for the variety of different agent types that we see out there. So single agents, agent swarms, supervisor agents, there's some other ones as well. We want to make it really easy for anyone who doesn't understand agents or is coming to it from an engineering background to easily get started with these common architectures.

At the next level, we want to make it possible for people who are on these product engineering teams but maybe not developers themselves to be more involved in building agents. So, one of the coolest things that we launched maybe a year ago at this point is *LangGraph Studio*. And so today we're excited to give it a facelift.

We're launching Langrass Studio V2. Uh no more desktop app so you can run it if if if you're not on Mac anymore. Um and it comes with a bunch of improvements as well. So you can see all the LM calls in a playground directly in the studio. You can build up data sets here. You can you can modify prompts as well.

So you can start to modify the agent and and I think most excitingly is you can pull down production traces from Langmith into your local langraph studio so that you can start to modify the agent. It will then hot reload and then you can you can try to fix these production issues that you're seeing.

And then finally we want to make it possible for more and more people who aren't developers at all to build agents from scratch, not just on product engineering teams. And so when we think about folks at larger enterprises, there are often a number of tasks that they want to do and build agents for and and and it's tough to get kind of like engineering resources to start.

And so we want to make it more and more easy for folks to build agents in uh a no code way. And so today we're launching open source *Open Agent platform*. It's powered by Langraph platform. It uses agent templates to allow people to build agents in a no code way. It comes with a tool server that uses MCP. It comes with Rag as a service so you can easily get started with anything related to Rag and it contains an agent registry so that you can see all the different agents that you've created. And so this is open source. You can check it out today.

#### Belief #6: Deployment of the Agents is the next hurdle

And finally, the last belief we have is that deployment of agents is the next hurdle.
So, it's possible to build agents. We we've we've we've talked about what it looks like. Once you build an agent, you then need to deploy it. And and and and sometimes this can be easy. Sometimes you can stand up kind of like a traditional kind of like web server and put it behind it. But we see more and more that agents are looking a little bit different than traditional web apps.

So, specifically, they're often *long running*. We see agents, deep research is a great example, that takes 10 minutes to run. We see agents that are taking an hour or 12 hours to run. They're often *bursty* in nature. So, especially if you kick them off as background jobs, you might be kicking them off hundreds or thousands at a time and they're *flaky*.

They're flaky in a bunch of different ways. The, you know, the calls to the LLM might fail, but also you want to have human in the loop because these LLMs might not do what you expect. And so, you need some statefulness in these agents to allow this human in the loop or human on the loop interaction patterns. And so we we've seen these patterns crop up.

(20:48) We think that agents are going to become more and more longunning, more and more bursty, and more and more stateful. And so we want to help people tackle this deployment challenge. And so *Langraph Platform* we launched in beta about a year ago and today we're excited to announce that it's officially generally available. So what's in Langraph platform? If you haven't checked it out, there are 30 different API endpoints that we stand up for everything from streaming to human in the loop to memory.

It scales horizontally so it can handle burstiness. It's designed for these longunning workloads and you can actually expose the agents that you deploy here as MCP servers. It also comes with a control plane where you can discover the agents that everyone at your or has deployed. You can share agents. You can reuse these agents with templates.

And then there are a few different deployment options. So we have a cloud SAS offering as well as hybrid and then fully self-hosted options.

## Resources

- [LangChain Interrupt 2025](https://interrupt.langchain.com)
- [Interrupt 2025 Keynote - Harrison Chase (LangChain) - YouTube](https://www.youtube.com/watch?v=DrygcOI-kG8)

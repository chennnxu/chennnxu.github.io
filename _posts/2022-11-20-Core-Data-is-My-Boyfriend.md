---
layout: post
title: Core Data
subtitle: Part 1 Foundations
tags: [iOS development, framework, core data]
comments: true
---

# Section 1 Introduction

Hello everyone,  we will embark on a new journey and learn a new way to persist our data -- Core Data. Users expect to find their data each time they launch their applications, Core data framework helps you ensure that they will. Apple’s Core Data provides a versatile persistence framework.

We're going to be diving into Core Data, including the foundamentals, some advanced features.  We build a core data based application "To do list Application" and then dissects the most important parts of its Core Data related code to show what they do and how they interact. Especially, walk you through how we can perform all of the CRUD operations using Core Data. 

# Section 2 Core Data Foundamentals

## 2.1 A little bit history about core data

In the early 1990s, **Object-oriented programming** become the dominant programming paradigm. But working with objects created a problem, developers had to convert query results from tables or two-dimensional data structure (e.g. SQL databases) to objects. Engineers in **NeXT** which was a company founded by Steve Jobs developed a framework called “Enterprise Objects Framework” (EOF), which was supposed to solve the problem mapping their results to objects. Apple purchased NeXT and launched "Cocoa" and also the **Core Data framework**. Some of its code was based on EOF Objective-C code. 

By the way, NeXT also developed NeXTSTEP – an OS that was the foundation for OS X and iOS. . NeXTSTEP initials are NS – that’s why many classes in the Objective-C Foundation Framework have the prefix “NS,” because they were part of NeXTSTEP OS.

## 2.2 what core data is and isn't?

We must start our journey with the expected one-million-dollar question –
what is Core Data?

### Is

Core Data is the M in MVC, the model layer of your application. Core Data not only is an extensive framework but also represents the data layer, and as a result, it plays a significant role in your app architecture [Unleash Core Data]

Core Data is first and foremost an object graph manager [Zarra, M. (2016). Core Data in Swift: Data Storage and Management for IOS and OS X. *Core Data in Swift*, 1-214.]

### Isn't

Core Data isn’t the only data storage option, nor is it necessarily the best option in all scenarios. [Pro Core Data] Core Data performs best when its role is to be your app data layer and serve the app business logic. [Unleash Core Data]

Core Data is not a database. Although Core Data can store data in a relational database (such as SQLite), it is not a database engine. [Pro Core Data] 

## 2.3 How Does Core Data Work?

It's important to understand how the various classes that make Core Data tick play together, or put another way, how does core data work? 

There are a lot of new terms in Core Data. What I want to mention here is a basic and important concept -- **NSManagedObject**. Just remember, when we're talking about entities, we're talking about the table (class). When we're talking about attributes,  we're talking about the columns in the table (properties of the class). And when we're talking about NSManagedObject, then we're simply talking about every single row in our table that is filled with data. All of the properties and relationships defined in our data model are available and are easy to access directly from the NSManagedObject.

The heart of the Core Data framework is Core Data Stack. Let's see this figure from Aplle Documentation. (More detailed about container, model, context, coordinator can be found on Apple Documentation)

As a user of Core Data, you should never interact directly with the underlying persistent store. You should try to picture Core Data as a framework that manages the persistence of objects rather than thinking about databases. Much like we need a livable environment to subsist, managed objects must live within an environment that’s livable for them, usually referred to as a managed object context, or simply context. The managed data model can also describe the relationships between those entities. A coordinator that uses the model to help contexts and persistent stores communicate.

## 2.4 How to Work with Core Data?

After knowing what is core data and how it works,  we need to learn how to setup and configure our core data data model in order to use it in our projects.

The first thing if you remember is that when we choose a template create a new project.  There's a checkbox says "Use Core Data", select the checkbox, some files automatically gets created by Xcode. Sometimes you don't know that you need to persist your data using Core Data, or you realize that you need core data after create the projects, you can also add core data to any project even at a later date.

... to be continued

## Stay Tuned on Part 2 ;)

# Reference

[1] Zarra, M. (2016). Core Data in Swift: Data Storage and Management for IOS and OS X. *Core Data in Swift*, 1-214.

[2] Privat, M., & Warner, R. (2011). Pro Core Data for IOS. Springer.

[3]  https://developer.apple.com/documentation/coredata

[4] A Tsadok. (2022). Unleash Core Data. Springer.

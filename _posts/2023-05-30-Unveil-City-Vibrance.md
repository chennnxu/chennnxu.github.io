---
layout: post
title:  Unveiling City Vibrance
subtitle: Events analysis of Berlin with Eventbrite
cover-img: /assets/img/berlin-event.jpg
tags: [Sunday Project, Data Analysis]
comments: true
---

### Introduction

Social events have increasingly become significant indicators of cultural and social dynamics within cities. Social events serve as platforms for community engagement, cultural expression, and tourism promotion. Understanding the dynamics and characteristics of social events can provide valuable insights into city cultural landscapes and social fabric.

Eventbrite platform serves as a comprehensive source of event data, capturing a wide range of events across various cities. This research aims to create a city portrait of Berlin by analyzing social event data obtained from the Eventbrite platform. This research will address the following research questions:<br>
**RQ1**: What are the event time modes? <br>
**RQ2**: What are the event category segments? <br>
**RQ3**: How can event sentiment be segmented? <br>
**RQ4**: How can event networks be modeled and analyzed, and what insights can be derived from them? (*)

### Data
The Eventbrite API provides a comprehensive set of functionalities that enable developers to leverage the platform's features programmatically. 
To collect all events and their event IDs in a specific city, I will scrape the Eventbrite website as the API does not offer such functionality. For example, to gather specific metadata for the event "Finding Product-Market Fit: Berlin vol. 2," I obtained the Event ID '627139961507' from its dedicated webpage on Eventbrite. By utilizing the Event ID, I accessed the Eventbrite API to retrieve additional relevant information. 

The data was collected on May 30th, but due to a bug on Eventbrite, only 50 pages of events(total 999 events, from 2023-06-06 to 2023-11-16) can be accessed out of the total 100+ pages of events. The analysis cannot provide a definitive conclusion due to the limited availability of data, but the value lies in the underlying idea. If an ideal dataset becomes available in the near future, a reassessment will be conducted. The full scrapped data can be accessed on [Github](https://github.com/chennnxu/eventbrite/tree/29263d81ee27797d60ee31f141c1946fd6e095eb/data).

### Analysis and Preliminary Result

After processing the data, analysis is conducted based on the research questions. The expected results include:<br>
(1) Identification event time modes, highlighting temporal dynamics.<br>
(2) Segmentation and comparison of event categories, revealing the diversity of cultural and social events.<br>
(3) Segmentation and comparison of event sentiment, offering insights into the sentiment of events.<br>
(4) Modeling and analysis of event networks, uncovering key influencers, communities, and interconnections within the social event landscape.(*)

The main python packages and API used in this analysis including:
<mark>
requests, BeautifulSoup, Pandas, eventbrite etc.
</mark>

#### 



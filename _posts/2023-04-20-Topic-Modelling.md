---
layout: post
title:  Journey to PyConDe & PyData Berlin 2023
subtitle: Topic Modeling of Sessions
cover-img: /assets/img/berlin.jpg
tags: [Conference, NLP]
comments: true
---

<!-- # Topic Modeling of [PyConDe & PyData Berlin 2023](https://2023.pycon.de/) Sessions  -->



![](1.png)
![](2.png)
![](3.png)
![](4.png)


As a first-time attendee of such a great conference, I would say I am so lucky to get the grant provided by the Diversity Committee. It made it possible for me to attend this event and gain valuable insights into the latest trends and innovations in the field and make connection to over 1200 people with same interets. That's amazing!

After back from the event, I think why not using the new things you learned from the conference to make a summary of it. I am going to use spaCy to do topic modelling for all the session in PyConDe & PyData Berlin 2023.

```
# import packages
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
sns.set()
import spacy
import pyLDAvis.gensim_models
pyLDAvis.enable_notebook()# Visualise inside a notebook
import en_core_web_md
from gensim.corpora.dictionary import Dictionary
from gensim.models import LdaMulticore
from gensim.models import CoherenceModel
```

Topic modeling is an unsupervised machine learning technique that extract hidden topics from text. The algorithm I am going to use is LDA.

Step 1 get the data - done

Step 2 tokenization 

Step 3

Step 4 Candidate topics

Step 5 Topic distribution



# ADA

## Abstract

LGBTQ  This topic has been discussed in different media and is reflected in the given Quotebank dataset. The goal of our project is to find out the situation and law of LGBTQ through the analysis of the dataset, thereby predicting what kind of background LGBTQ can be better accepted and recognized by society. Firstly, we recognize the LGBTQ topics using sentence grammar analysis, then we derive the distribution statistics of LGBTQ, with related to other variables such as time, media and speaker background (e.g. gender, nationality, education background), and then analyze the sentimental factor of the quotation related to LGBTQ. The analysis section will then leave space for a more important chapter of our story: whether people's feelings and attitudes towards LGBTQ are related to the quotation time, speaker's country and other information. We can even dig out the relationship between LGBTQ and economic development of the world. Further, we also want figure out the reasons behind frequency changes towards LGBTQ topics, such as some important events at that time. This combined effort can help us have a deeper understanding on people's acceptance of LGBTQ under different backgrounds, thus we can make predictions for the future LGBTQ development and give suggestions for constructing a more equal and LGBTQ-friendly world community.



## Research questions

* How does the frequency of the LGBTQ topic change year after year, and what might be the reason for the change.
* How do people from different groups (e.g. gender, occupation etc.) talk about LGBTQ equality problems (positive or negative). Specifically, is there any correlation between a country's situation (citizens' average education level, GDP, GDP per capita) and the attitudes of their people toward this topic.
* How does the pattern of the distribution of speaker features change over time, and what might be the reason accounting for it. For example, does male people become more and more realized the LGBTQ topic than before?
* What are the topics that often co-occur with LGBTQ, and the reasons for those co-occurrence. Specifically, consider those topics that co-occur with LGBTQ, does it current has a positive or negative effect toward LGBTQ.
* How can we improve the situation based on the analysis of above RQs and existing information of QuoteBank.



## Dataset

#### Quotebank dataset

Quotebank is a dataset of 178 million unique, speaker-attributed quotations that were extracted from 196 million English news articles crawled from over 377 thousand web domains between August 2008 and April 2020. The quotations were extracted and attributed using Quobert, a distantly and minimally supervised end-to-end, language-agnostic framework for quotation attribution. In our analysis, we decide to use Quotation-centric data from 2015-2020 where the quotations are aggregated across all their occurrences in the news article data, and assigned a probability for each speaker candidate. 

URL: https://zenodo.org/record/4277311#.YY1yAi00jb0 

#### Speaker attributes dataset

These are external sources from Wikipedia for enriching Quotebank data, which contain the information of speakers’ features like gender, age, occupation and etc.

URL:https://drive.google.com/drive/folders/1VAFHacZFh0oxSxilgNByb1nlNsqznUf0

#### WBGAPI

WBGAPI provides modern, pythonic access to the World Bank's data API, which differs from other packages for World Bank data in a few respects and in general tries to take full advantage of the World Bank's powerful API while mitigating the impact of some its ideosyncracies. We will extract the GDP information from this dataset in order to analyze the correlation between country GDP and LGBTQ topic attention.

URL: https://deepnote.com/@carlos-mendez/PYTHON-Access-World-Bank-data-with-Python-fVexISvfTxO42ZUgyfinzA



## Methodology

- **Statistics analysis**: analyze quotation frequency distribution related to topics, time, speakers, media
- **Causation analysis:** figure out the causality between some big events and the variation of LGBTQ topic attention.
- **Correlation analysis** between country GDP and LGBTQ topic attention
- **Sentiment analysis** based on Google API
- **Acquiring co-occur topic clusters:** Apply BERT model embeddings and c-TF-IDF algorithm



## Proposed timeline

**29/10/2021:** 

Quotebank dataset preprocessing and overall analysis (analyze quotation frequency distribution related to topics, time, speakers, media) and build LGBTQ quotation dataset based on BERT topic extraction model.

**05/11/2021:** 

Building and preprocessing LGBTQ speakers feature dataset by merging speaker attributes (acquired from Wikipedia dataset, like gender, education level, nationality, etc.) with speakers who concern LGBTQ topics in Quotebank.

**12/11/2021:** 

Analyzing the correlation between country GDP and LGBTQ topic attention based on the WBGAPI dataset and Quotebank dataset.

**19/11/2021:** 

Applying BERT model embeddings and c-TF-IDF algorithm to get co-occur topic clusters.

**26/11/2021:** 

Using causation analysis to figure out the causality between some big events and the variation of LGBTQ topic attention.

**03/12/2021:** 

Analyzing speaker’s sentiment toward specific topic based on Google API.

**10/12/2021:**

Coming up with several visualization methods for the results we have already found above, in order to show all the findings to our readers.

**17/12/2021:** 

Preparing reports and final presentation of our data story.



## Organization within the team
**Duo Xu:** 
1.Quotebank dataset overall analysis (analyze quotation frequency distribution related to topics, time, speakers, medias).
2.Exploring if Google API could work for sentiment analysis
3.Analyzing speaker’s sentiment toward specific topic based on Google API.

**Guosheng Feng:** 
1.Build LGBTQ quotation dataset based on BERT topic extraction model
2.Exploring if BERT model embeddings and c-TF-IDF algorithm could work for further work.
3.Applying BERT model embeddings and c-TF-IDF algorithm to get co-occur topic clusters.

**Aibin Yu:** 
1.Building and preprocessing LGBTQ speakers features dataset
2.Exploring if WBGAPI dataset could work for further work.
3.Analyzing the correlation between country GDP and LGBTQ topic attention based on the WBGAPI dataset and Quotebank dataset.

**Yifeng Chen:** 
1.Quotebank dataset preprocessing
2.Writing the proposal of milestone2.
3.Using causation analysis to figure out the causality between some big events and the variation of LGBTQ topic attention.

We will use visualization methods to present our final work, prepare reports and presentation.


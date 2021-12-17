# Don’t neglect, let rainbow shining!

## Abstract

Do you know there are still 69 UN member States criminalizing consensual same-sex activity? During the Covid-19 pedantic, LGBTQ people are struggling to survive in a world that has become even more unequal and violent. What can we do to change this situation? Well, we believe the answer may lie in the QuoteBank dataset. The LGBTQ topic has been discussed in different media and reflected in the given Quotebank dataset. In this project, we will go through the dataset and try to find out what we can do to help better their situation. Firstly, we recognize the LGBTQ topics using sentence grammar analysis, then we derive the distribution statistics of LGBTQ, with related to other variables such as time, media, and speaker background (e.g. gender, nationality, education background), and then analyze the sentimental factor of the quotations related to LGBTQ. 

Moreover, we extract the correlation and causations of other factors and learn how they affect equality in human society and the development of LGBTQ society. Further, we also want to figure out the reasons behind frequency changes towards LGBTQ topics, such as some important events at that time. This will give us a deeper understanding of people's acceptance of LGBTQ under different backgrounds, thus we can make predictions for the future LGBTQ development and give suggestions for constructing a more equal and LGBTQ-friendly world community.

## Research questions

- How does the frequency of the LGBTQ topic change year after year, and what might be the reason for the change?
- How do people from different groups (e.g. gender, occupation, etc.) talk about LGBTQ equality problems (positive or negative)? Specifically, is there any correlation between a country's situation (citizens' average education level, GDP, GDP per capita) and the attitudes of their people toward this topic?
- How does the emotion pattern of the distribution of speaker features change over time, and what might be the reason accounting for it. For example, do male people become more and more postive toward the LGBTQ topic than before?
- How can we improve the situation based on the analysis of the above RQs and existing information of QuoteBank?

## Dataset

#### Quotebank dataset

Quotebank is a dataset of 178 million unique, speaker-attributed quotations that were extracted from 196 million English news articles crawled from over 377 thousand web domains between August 2008 and April 2020. The quotations were extracted and attributed using Quobert, a distantly and minimally supervised end-to-end, language-agnostic framework for quotation attribution. In our analysis, we decide to use Quotation-centric data from 2015-2020 where the quotations are aggregated across all their occurrences in the news article data, and assigned a probability for each speaker candidate. 

URL: https://zenodo.org/record/4277311#.YY1yAi00jb0 

#### Speaker attributes dataset

These are external sources from Wikipedia for enriching Quotebank data, which contain the information of speakers’ features like gender, age, occupation, etc.

URL:https://drive.google.com/drive/folders/1VAFHacZFh0oxSxilgNByb1nlNsqznUf0

#### [**WorldBank**](https://data.worldbank.org/):

  WorldBank data contains various of statistical data from different countries and regions over the world, such as economy, education, employment, environment and population. This dataset maintains a number of macro, financial and sector databases where much of the them comes from the statistical systems of [member countries](http://www.worldbank.org/en/about/leadership/members).

  We mainly use worldbank data for analyzing the factors that lead to different acceptance levels towards LGBTQ community of different countries and regions.

#### [**Sexual Orientation Laws in the World**](https://www.kaggle.com/mpwolke/cusersmarildownloadsomophobiacsv):

  This dataset maintains different LGBTQ-related national policies of different countries, such as same-sex marriage, conversion therapy, penalty, adoption & fostering and employment protection of LGBTQ people. The data mainly from ILGA World along with the State-Sponsored Homophobia report.

  We use this dataset for evaluating LGBTQ acceptance levels of different countries. By quantifying the policies into scores, we combine it with the WorldBank dataset for regression analysis of different factors.
## Methodology

- **Statistics analysis**: analyze quotation frequency distribution related to topics, time, speakers, media
- **Correlation analysis** First, we conduct the regression analysis for different regions in the world, and choose the independent variable to be GDP per-capita instead of overall GDP score,Second, we explore the relationship between the education level and acceptance of LGBTQ, we conduct the regression analysis between the education ratio for population over 25 years old and the LGBTQ accenptance score.
- **Sentiment analysis** After acquiring the speakers with their corresponding features, we will need some sentimental analysis tools to check the speakers' attitudes towards LGBTQ. For this part we will use google cloud's natural language api. The analyze_sentiment function will return a score and a magnitude for the given quotation. Then we divide the emotion of each quotation into 4 groups(positive, negative, mixture, neutral). First, we analyze the total emotion distribution of the whole quotebank dataset related to LGBTQ topic. Next, we use different features to divide people into several groups, for example, if we choose the feature as age, there are 3 groups: young(born after 1990), middle of age(born in 1960-1989), old(born before 1959), then we analyze the distribution of each group.
- **Acquiring co-occur topic clusters:** 
- Here we analyze the topics that co-occur with LGBTQ.

Instead of what we have done in the frequent topic extraction phase, here we want to be more precise and convincing about the topics that we extracted. Further, we want give more reasoning to them, and one way for doing this is to use topic aggregations. Here we directly apply the intergrated API as **BERT-Topic**, whose method scheme is as follows:

1. Gather LGBTQ quotations as one document (lists of quotations)
2. Performing text embedding using Transformer language models (with pretrained weight loaded)
3. Apply aggregation algorithm to text embeddings using UMAP (for dimension reduction) and HDBSAN (for clustering) algorithm
4. extract topics using class-based TF-IDF algorithm

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

Coming up with several visualization methods for the results we have already found above, to show all the findings to our readers.

**17/12/2021:** 

Preparing reports and final presentation of our data story.

## Organization within the team

**Duo Xu:** 

-  Quotebank dataset overall analysis (analyze quotation frequency distribution related to topics, time, speakers, media). 
- Exploring if Google API could work for sentiment analysis 
- Analyzing speaker’s sentiment toward specific topic based on Google API.

**Guosheng Feng:** 

- Build LGBTQ quotation dataset based on BERT topic extraction model 
- Exploring if BERT model embeddings and c-TF-IDF algorithm could work for further work. 
- Applying BERT model embeddings and c-TF-IDF algorithm to get co-occur topic clusters.

**Aibin Yu:** 

- Building and preprocessing LGBTQ speakers feature dataset 
- Exploring if the WBGAPI dataset could work for further work. 
-  Analyzing the correlation between country GDP and LGBTQ topic attention based on the WBGAPI dataset and Quotebank dataset.

**Yifeng Chen:** 

- Quotebank dataset preprocessing 
- Writing the proposal of milestone2. 
-

**We will use visualization methods to present our final work, prepare websites.**


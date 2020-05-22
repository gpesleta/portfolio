---
layout: single
header:
  teaser: /assets/images/rappler_wordcloud.png
title: "unwRAPPLER: Identfying Underlying Themes in Rappler News Articles"
date:   2019-07-23 14:14:36 +0800
categories: projects
mathjax: "true"
excerpt: "This study aims to uncover the underlying themes of Rappler news articles via unsupervised clustering techniques and see if there is an inherent concentration of news in a specific theme."
---
<div><span style="background-color: #425564; padding-top: 100px; padding-right: 20px; padding-bottom: 50px; padding-left: 20px; color: #ffffff; font-size: 20px; font-weight: bold">EXECUTIVE SUMMARY </span></div>
Rappler, one of the leading online news publishers in the Philippines, seeks to inspire community engagement and create action for social change through citizen journalism. However, it has recently been under scrutiny by the Philippine government for “twisted” reporting. This study aims to uncover the underlying themes of Rappler news articles via unsupervised clustering techniques and see if there is an inherent concentration of news in a specific theme. A total of 11,079 articles were extracted from Rappler’s national news section published from January 2018 to May 2019. Features were extracted from the articles using a term frequency-inverse document frequency (TF-IDF) vectorizer and dimensions were reduced by implementing Latent Semantic Analysis (LSA). Lastly, unsupervised clustering via k-means algorithm was applied to group the articles and internal validation metrics were utilized to determine the optimal number of clusters. Ten clusters were uncovered, with Philippine President Rodrigo Duterte as the dominant cluster. The remaining themes touch on different branches of government, police and weather updates, and trending national issues. The insights gained from this research can aid Rappler in balancing its reporting by lessening bias towards specific topics.

<div><span style="background-color: #425564; padding-top: 100px; padding-right: 20px; padding-bottom: 50px; padding-left: 20px; color: #ffffff; font-size: 20px; font-weight: bold">INTRODUCTION </span></div>
Rappler is one of the leading online news publishers in the Philippines. It was started in 2011 by former CNN journalist Maria Ressa. However, since 2018, Rappler has been under heavy scrutiny by the Philippine government for “twisted” and “biased reporting” [[1](#ref1)].  Philippine President Rodrigo Duterte even went so far as calling Rappler a “fake news” outlet that publishes articles that are “pregnant with falsity” [[2](#ref2)]. Rappler has been on the receiving end of criminal cases from the Philippine governments. BIR filed several counts of tax evasion charges against Rappler CEO Maria Ressa. Cyber-libel cases were also filed against Ressa.

Why is Rappler being targeted by the Duterte Administration? Is Rappler “twisted” and “biased” in its reporting? In this work, we uncovered the underlying themes of Rappler’s news articles via unsupervised clustering, to see if there is indeed an inherent concentration of news in a specific topic or theme.

<div><span style="background-color: #e76229; padding-top: 100px; padding-right: 20px; padding-bottom: 50px; padding-left: 20px; color: #ffffff; font-size: 20px; font-weight: bold">BUSINESS VALUE </span></div>

Extracting themes from a set of articles programmatically has a widespread application in the digital publishing industry and can be used to deliver business value to readers, journalists, advertisers, aggregators, and researchers.  

- **Readers** in the digital age have no patience. They are more likely to use a search engine to retrieve a set of ranked articles from multiple news sources and it becomes a challenge for online news platforms to engage a reader continuously. Automatic theme extraction and clustering of articles provide the ability to structure a set of articles to make it easier for readers to navigate to related articles. If articles can be presented in a logical hierarchy driven by patterns in the data, human intervention is minimized (saving on labor costs) and the reader is kept on the news platform, increasing engagement time on the site.

- **News Publishers and Journalists** seeking to address topics of broad interest to their readership can benefit from a thematic clustering of articles to determine the balance of news coverage. Publishing organizations are always looking for gaps in news coverage to offer readers some perspective and insight into topics that are not heavily covered. By examining existing themes holistically, they can better gauge what is missing and what their next article should be about. 

- **Advertisers** that are considering online news platforms to reach specific customer segments can tailor their messages so that they are congruent with the themes that readers are interested in. For instance, themes dealing with legislative or judicial proceedings may appeal to advertisers whose clients are lawyers or law schools.  Advertisers of tourism and tourist agencies may be interested in weather and specific vacation destinations, such as Boracay. 

- **Aggregators** in the licensed publishing industry create packages of content for redistribution. Their business model, which can be subscription or advertiser-based, is to target specific customers based on their geographic, demographic, and psychographic profile. For instance, if an investor wanted to understand market conditions for a particular industry, they would subscribe to a real-time news delivery service that was able to provide the relevant articles.

- **Researchers** make money by selling analytical reports. By studying the themes presented on news platforms and combining the study with other metrics such as readership engagement, sentiment analysis, and political stance, they can make in-depth comparisons with other news delivery platforms to better inform advertisers and aggregators.

<div><span style="background-color: #425564; padding-top: 100px; padding-right: 20px; padding-bottom: 50px; padding-left: 20px; color: #ffffff; font-size: 20px; font-weight: bold">METHODOLOGY </span></div>

To uncover the underlying themes, a total of **11,079 news articles** published from **January 2018 to May 2019** were retrieved from Rappler's Nation section (`https://www.rappler.com/nation`). The general workflow for clustering the Rappler articles as shown in [Figure 1](#fig1) involves the following steps:

1. Data Extraction
2. Data Storage
3. Data Preprocessing
4. Exploratory Data Analysis
4. Feature Extraction via TFIDF Vectorization
5. Dimensionality Reduction using Latent Semantic Analysis (LSA)
6. Unsupervised clustering using *k*-means algorithm

![Figure 1. Workflow for clustering the Rappler articles]({{ site.url }}{{ site.baseurl }}/assets/images/rappler_methodology.png)

Each step of the workflow will be discussed in the succeeding sections. 

<div><span style="background-color: #425564; padding-top: 100px; padding-right: 20px; padding-bottom: 50px; padding-left: 20px; color: #ffffff; font-size: 20px; font-weight: bold">REFERENCES </span></div>
[1] <a id='ref1'></a>"Duterte says he banned Rappler due to 'twisted' reporting", https://www.rappler.com/nation/197230-duterte-rappler-ban-twisted-reporting

[2] <a id="ref2"></a>"Duterte calls Rappler 'fake news outlet", https://www.rappler.com/nation/193806-duterte-fake-news-outlet

[3] https://towardsdatascience.com/all-the-news-17fa34b52b9d

[4] https://seangtkelley.me/blog/2018/01/03/news-article-clustering

[4] https://scikit-learn.org/stable/auto_examples/text/plot_document_clustering.html#sphx-glr-auto-examples-text-plot-document-clustering-py

[5] http://www.scholarpedia.org/article/Latent_semantic_analysis
# Mind the Negativity - Media Coverage of the European Refugee Crisis

Luis Rei, Evgenia Belyaeva, Dunja Mladenić, Gregor Leban

[Website](https://lrei.github.io/negativity/)

## Abstract
The media has played a crucial role in covering the ongoing European refugee
crisis. In this work, we analyse the coverage of the crisis using an approach
that combines media studies and text mining. Our analysis is based on a dataset
of more than 7000 articles published by 13 well-known news outlets from
different countries between January 2015 and June 2016. We present three main
research hypotheses; provide evidence to support them and a detailed methodology.
First, we notice that the number of articles published correlates highly with
the number of refugees showing a correlation coefficients greater than 0.8 for
refugees coming from Syria and Iraq. Second, those articles are predominantly
(> 80%) negative in outlook. Third, there are notable differences in reporting
among publishers that can be attributed to their political affiliation.
Moreover, the considered American publishers, although with less number of
articles, turned to be far more negative than the considered European publishers.

Keywords: Europeanrefugee crisis, negativity, mass media, news, social dynamics,
Event Registry, text mining, active learning


## Data
The data consists of news articles published online between Jan 2015 and Jun
2016 by:

* www.bbc.co.uk
* www.aljazeera.com
* www.theguardian.com
* www.independent.co.uk
* www.cnn.com
* www.dw.com
* www.usatoday.com
* www.thelocal.de
* www.nytimes.com
* www.thelocal.it
* www.dailymail.co.uk
* www.foxnews.com
* www.wsj.com


Only articles with certain words (see paper) were collected.

|Published | Collected | Manually Labeled |
|----------|-----------|------------------|
| 1,334,212| 8,331     | 1,573            |
-------------------------------------------
Table: Total articles published by selected publishers in the time period,
articles collected using keywords, and manually labeled articles.


Not all of the articles collected using keywords were actually relevant to the
European Refugee Crisis (e.g. some talked about refugees arriving in Canada,
...). We deal with those issues in the paper.


## Hypothesis


## Main Findings


### More Refugees More News

| Source Country | Pearson Correlation Coefficient | p-value | t-value |
|----------------|---------------------------------|---------|---------|


### Prevalence of Negative News
blah

### Negativity Depends on Publisher
blah


## Download The Dataset
[Download Dataset](https://drive.google.com/file/d/0B3CDC49Z2hjxRk13bGl1WThVblk/view)

There are 3 files:

* relevant.csv: news articles labelled with relevant/not relevant;
* negativity.csv: news articles labelled with Negative/Positive;
* unlabeled.csv: unlabelled articles;
* stopwords.txt: stopwords used in the text classifiers;


This dataset contains the following fields (labels in their respecitive files):

* **date**: the date the article was published in;
* **source**: the URL of the publisher of the article;
* **title**: the title of the article;
* **url**: the URL where the article contents were retrieved from;
* **relevant**: the relevant (label) of the article Relevant or Not Relevant
  (Irrelevant);
* **negativity**: the negativity (label) of the article Positive or Negative;
* **split**: the split for the article train, dev, test.


# Mind the Negativity - Media Coverage of the European Refugee Crisis

[Luis Rei](http://luisrei.com), Evgenia Belyaeva, [Dunja Mladenić](http://ailab.ijs.si/dunja/), Gregor Leban

email: {firstname.lastname}@ijs.si


This [Website](https://lrei.github.io/negativity/) provides a summary of
the paper and makes available the dataset used in the paper. To download it,
follow the link at the end of this page.

For a better presented, complete view, the methodology, details, discussion,
etc read the paper:

**Mind the Negativity - Media Coverage of the European Refugee Crisis** - Luis
Rei, Evgenia Belyaeva, Dunja Mladenić, Gregor Leban, _**Not yet published**_


This work made use of [Event Registry](http://eventregistry.org) which collects and
annotates in real-time news articles published by over 30,000 news publishers
worldwide.


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

Keywords: European refugee crisis, negativity, mass media, news, social dynamics,
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

Table: Total articles published by selected publishers in the time period,
articles collected using keywords, and manually labeled articles.


Not all of the articles collected using keywords were actually relevant to the
European Refugee Crisis (e.g. some talked about refugees arriving in Canada,
etc). We deal with those issues in the paper.


## Hypothesis


## Main Hypothesis and Findings


### More Refugees More News
The number of articles published about the European refugee crisis is highly
correlated to the number of refugees arriving in Europe.


| Source Country | Pearson Correlation Coefficient | p-value | t-value |
|----------------|---------------------------------|---------|---------|
|Total (Non EU28)| **0.70**                        | 1.8E-3  | 3.78    |
|Syria           | **0.81**                        | 6.8E-5  | 5.44    |
| Afghanistan    | 0.52                        | 3.3E-2  | 2.35    |
| Iraq           | **0.85**                    | 1.6E-5  | 6.23

Table Correlation between the monthly aggregate of the number of articles
classified “Relevant” and the Eurostat numbers for first time asylum
applications, total and broken down among the top 3 applicant source countries.
Statistically significant correlations in bold.


[[https://raw.githubusercontent.com/lrei/negativity/gh-pages/relevant_vs_asy.png|alt=”News articles published vs Asylum Applications”]]

Figure: Asylum Applications vs. Relevant Articles Published per month in our
dataset.


### Prevalence of Negative News

News outlets strongly prefer to publish articles that follow a negative
narrative when covering the European refugee crisis.

The variation in the split between negative and positive coverage seems to be
highly influenced by social dynamics associated with key events such as the
“The Death of Alan Kurdid” or the “Charlie Hebdo shooting”. Notably, the reaction
to the former resulted in month with the lowest negativity in our data.


[[https://raw.githubusercontent.com/lrei/negativity/gh-pages/negativity_month%2Bevents.png|alt=”Negative vs Positive articles published per month (%).”]]

Figure 6: Negativity (%) per month i.e. the percentage of total articles,
published during each month that was classified as negative. Annotated with
influential events: positive in green, negative in red. Note: Graph starts
a 50% not 0%.


| Class      | Keywords |
|-----------------------|
| Negative | problem, police, claim, muslim, fear, illegal, security, attack, violence, vessel, racist, smuggle, refuse, tent, unaccompanied, boat capsize, criminal gang, border fence |
| Positive | help, project, reunite, win, open, artist, exhibition, donate, pope, documentary, opportunity, compete, player, solidarity, volunteer, refugee welcome, reunite family     |

Table: Examples of automatically extracted keywords from news articles classified Negative and Positive.



### Negativity Depends on Publisher
Conservative-leaning publishers being even more negative. The American
publishers, although with less articles, turned out to be more negative than
European publishers.

We saw no evidence of a concerted effort to refer to refugees as “migrants”.
Rather, there seem to be a tendency or an enduring confusion among most of the
publishers in their use words “migrant” and “refugee” interchangeably.
According to UNESCO (UNESCO), the terms refugee, migrant and asylum seeker have
significantly different meanings. A refugee is a person who escapes his/her
country of origin because of the fear of being persecuted for reasons of race,
religion, nationality, armed conflict etc. A migrant is defined as a person who
lives outside of his country of origin either temporarily or permanently and
has developed ties to his new country.

Interestingly, German publishers, use the terms “refugee” and “Asylum seeker”
more often when compared to other publishers, which probably shows a more
welcoming attitude to the refugees, which is also in line with the political
stand on the refugee crisis in Germany during this period.


## Download The Dataset
[Download Dataset](https://drive.google.com/file/d/0B3CDC49Z2hjxRk13bGl1WThVblk/view)

If you use this data, please cite the paper.

There are 3 files:

* **relevant.csv**: news articles labelled with relevant/not relevant;
* **negativity.csv**: news articles labelled with Negative/Positive;
* **unlabeled.csv**: unlabelled articles;
* **stopwords.txt**: stopwords used in the text classifiers.


This dataset contains the following fields (labels in their respecitive files):

* **date**: the date the article was published in;
* **source**: the URL of the publisher of the article;
* **title**: the title of the article;
* **url**: the URL where the article contents were retrieved from;
* **relevant**: the relevant (label) of the article Relevant or Not Relevant
  (Irrelevant);
* **negativity**: the negativity (label) of the article Positive or Negative;
* **split**: the split for the article train, dev, test.


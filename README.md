# negativity
Mind the Negativity - Media Coverage of the European Refugee Crisis.

Luis Rei, Evgenia Belyaeva, Dunja Mladenić, Gregor Leban


### Data
The data consists of news articles published online between Jan 2015 and Mar
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


Only articles that met certain criteria (see paper) were collected.


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


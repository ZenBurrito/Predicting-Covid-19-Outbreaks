# Predicting-Covid-19-Outbreaks
Using tweets to predict Covid-19 Outbreaks

## Overview

Data used in this project came from Kaggle, the CDC, Google Trends, and Twitter. Using basic NLP libraries (NLTK, TweetTokenizer)

For the analysis of the tweets I started with a basic, mostly cleaned, dataset off of Kaggle to create text based predictors. I also gathered my own twitter data about vaccinations, which accounted for another 10000 rows. I used other libraries to clean the text ([TextHero](https://texthero.org/)), and then used a Trigram CountVectorizer. To create my target variable I used data from Google Trends and the CDC. Using percentages of new cases and trending relevance, I created a score between the two that accounts for not only physical outbreaks, but a social one as well.


## Business Problem & Understanding

Covid-19 is a problem that does not need much introduction or explanantion, however, for this project I wanted to find if there was any correlation between twitter behavior and possible outbreaks. This is important to understand because this could help hospitals better prepare for a response to an outbreak. This could also be applicable to anybody wanting to avoid close contact with the disease, giving them warning beforehand, which they can then use to make more informed decisions on how to handle their day to day.

## Data Understanding

My data came from multiple sources, First I started with a base, almost cleaned, Kaggle dataset that had about 170k rows of tweets, for the sake of time and computational effectiveness, I trimmed down the dataset so I had more time for model tuning and other aspects of the project. I also gathered another 11k rows of tweets that were about vaccinations. Those two datasets were both used to create text based predictors using a CountVectorizer, to see if there was any direct correlation between the tweets and my target variable.

The target variable was constructed with both data from Google and the CDC. I created a score using the percentages of new cases as well as the relevance of searches. I then scaled the score down so outliers did not effect them as much. This accounts for not only physical outbreaks, but the social aspect as well.

## Data Preparation

Doing self research I stumbled upon an NLP library called [TextHero](https://texthero.org/), and the steps they take to clean out text data. I also used a TweetTokenizer made specifically for Twitter data. 

## Modeling

After taking an iterative modeling approach, I found that one model performed exceptionally better than other models. Using the Multinomial Naive Bayes model I was able to predict outbreaks at a ___ percent accuracy. Part of the reason the Naive Bayes worked better than other models is because it assumes independence between my variables, meaning each of them is counted on its own without any weights, this pairs well with a CountVectorizer because it gives us a word count.


## Conclusions & Next Steps

My model was able to predict __ percent accurate. I believe that through more data I could come to a more conclusive result on whether there is a direct correlation between tweets and covid-19 outbreaks. I would also like to start collecting data from other social media sites, ones like Facebook and Reddit are both places where highly opinionated people tend to go, therefore they're more likely to use key words that would indicate whether or not an outbreak is going to happen.

```
├── README.md                 <- The top-level README for reviewers of this project
├── Final_notebook.ipynb      <- Narrative documentation of analysis in Jupyter notebook
├── presentation.pdf          <- PDF version of project 
├── Images                    <- Generated from code
├── Data                <- Older notebooks, kept to see progress
```

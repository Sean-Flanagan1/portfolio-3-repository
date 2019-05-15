# Project 3: Web APIs & Classification

# Problem Statement

How can we accurately predict which subreddit a post came from based on the text of the post?

# Executive Summary

The goal of the project is to create a classification model that will predict which subreddit a post belongs to on reddit.com. The two subreddits for my model are r/baseball and r/marchmadness. I chose to use the title text to predict whether a post was in r/baseball or r/marchmadness. I obtained 924 title posts from r/baseball and 811 title posts from r/marchmadness. I then cleaned the data by removing null values and duplicates. I merged the dataframes into one dataframe. Afterwards, I used my models to access the accuracy of the model predictions.

## Models:

I created two models. My first model was logistic regression and the second model was multinomial naive bayes. In each model, I gridsearched for hyperparameters. For each model I also tokenized the data. I count which model performed better with count vectorization and tfidf vectorization. 


# Data Dictionary

| Feature | Type | Description |
| --- | --- | --- |
| subreddit | Obj | r/baseball or r/marchmadness |
| title | Obj | Text from the title of the post |

# Conclusion

The logistic regression tfidf vectorizer performed the best out of the other models. The accuracy was 91.24%. The logistic regression count vectorizer accuracy score was 91.01%. The tfidf vectorizer performed better than the countvectorizer at 90.55% compared to 88.71%. Overall it appears that tfidf was the best vectorizer. 

I would recommend to keep testing different models and vectorizers with reddit posts that have very similar words. While the logistic regression model with both vectorizers performed better than the mulinomial naive bayes model, I would recommend to continue to test both models with different subreddits. A greater sample size will be needed to understand which model performs better with reddit.

# Data Sources

Baseball Subreddit: https://www.reddit.com/r/baseball/
March Madness Subreddit: https://www.reddit.com/r/marchmadness/
Word Clouds: https://www.datacamp.com/community/tutorials/wordcloud-python
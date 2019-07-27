---
layout: project
type: project
image: "images/Mean Sentiment Analysis by Subreddit.png"
title: Subreddit Post Classification Model
permalink: projects/subreddit_classification
# All dates must be YYYY-MM-DD format!
date: 2019-07-12
labels:
  - Python
  - Logistic Regression
  - Natural Language Processing
summary: I used Reddit's API to collect posts from two subreddits, r/The_Donald and r/Republican. Using natural language processing (NLP), I trained a classification model to predict which subreddit a given post came from. Ultimately, my logistic regression model was able to classify a user post with 75% accuracy just by using the title data.
---
**Reddit pages chosen**
- https://www.reddit.com/r/Republican/
- https://www.reddit.com/r/The_Donald/

**From r/Republican Community Details**

"/r/Republican is a partisan subreddit. This is a place for Republicans to discuss issues with other Republicans."

**From r/The_Donald Community Details**

"The_Donald is a never-ending rally dedicated to the 45th President of the United States, Donald J. Trump."

These two subreddits bear some similarities and have some overlap. However, it's important to note that r/The_Donald has been quarantined recently for attempting to incite violence against police and other public officials, a violation of reddit's content policy. It is a well known and used alt-right subreddit. By contrast, r/Republican is a subreddit that should reflect contemporary Republican views. There is some explicit content posted on r/The_Donald. I believe a model like this could be very useful for understanding more about current partisan viewpoints.

## Results:

After pulling around 15,000 posts for each subreddit, I fit both a Gaussian Naive Bayes model and a logistic regression model to classify the reddit post titles. The logistic legression model ended up being the best of the two. It used ridge regression on term frequency–inverse document frequency (TFIDF) vectorized titles from the reddit data I pulled. It is important to note that performing sentiment analysis using the VADER and TextBlob python libraries did not help my model classify the posts any better. Ultimately, the logistic regression model was able to classify post titles by subreddit  about 75% of the time, which was a 25% increase over the baseline score.

# MADS Capstone 699 

## Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

We use the Reddit Comment Data between 2008 and 2019, a publicly available data set from clickhouse, to gauge the online opinion dynamics about iPhone. We have limited our data to two sureddits: Apple & iPhone. 
 The raw data can be accessed from this link: https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments. 

Specifically, our project contains three stages: (1) explore the online dynamics through topic modeling, i.e.,   extract the underlying themes/topics sourrounding iPhone to see the longitudinal change; (2) with 3380 posts sampled for manual sentiment labeling, we trained a classification model with those labeled data, then apply the best model to predict the sentiment (negative, neutral, positive) for remaining comment posts; (3) use monthly discussion volume (i.e., number of comments posted), the underlying topics as well aggregated sentiment strengh obtained in the first two steps, together with some external factors (e.g., GDP) to explore how social media would reflect or correlate with real-word business metrics (e.g., iPhone sales).

# MADS Capstone 699 

## Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

We use the Reddit Comment Data between 2008 and 2019, which is a publicly available data set from clickhouse, to gauge the online opinion dynamics about Apple and iPhone.  The raw data can be accessed from this link: https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments. 

Specifically, our project contains three parts: (1) explore the online dynamics with topic modeling to extract the underlying themes/topics sourrounding Apple and iPhone; (2) with 3380 posts sampled for manual labeling, we trained a classification model with those labeled data and then apply the best model to predict the sentiment embedded in all the remaining comment posts; (3) use the underlying topics as well aggregated sentiment strengh obtained in the first two steps, together with dicussion volumnes and other external factors (e.g., GPA) to explore how social media would reflect or correlate with real-word business metrics (e.g., iPhone sales).

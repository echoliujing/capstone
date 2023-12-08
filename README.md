# MADS699 Capstone   

## Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

We use the Reddit Comment Data between 2008 and 2019, a publicly available data set from clickhouse, to gauge the online opinion dynamics about iPhone. We have limited our data to two sureddits: Apple & iPhone. 
 The raw data can be accessed from this link: https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments. 

Specifically, our project contains three stages: (1) explore the online dynamics through topic modeling, i.e.,   extract the underlying themes/topics sourrounding iPhone to see the longitudinal change; (2) with 3380 posts sampled for manual labeling, we trained various classification model and apply the best model to predict the sentiment (negative, neutral, positive) for remaining comment posts; (3) use monthly discussion volume (i.e., number of comments posted), the underlying topics as well aggregated sentiment strengh obtained in the first two steps, together with some external factors (e.g., GDP) to explore how social media would reflect or correlate with real-word business metrics (e.g., iPhone sales).

To execute the codes, please follow the following steps:

(1) Topic Modeling: run the " " file.
(2) Sentiment Analysis: set up the environment by installing all packages listed in '2. requirements.txt' file, then run the "Sentiment classification.ipynb" file with the input data from the 'Labeled" folder (for model training and evaluation, included in this repository) and  "Data" folder (for prediction, not uploaded due to the limited repository storage), the output will be saved in a new folder named "Results" (not uploaded due to the limited repository storage).
(3) Offline Sales Prediction: run the " " file.

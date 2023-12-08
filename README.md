# MADS699 Capstone   

## Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

We use the Reddit Comment Data between 2008 and 2019, a publicly available data set from clickhouse, to gauge the online opinion dynamics about iPhone. We have limited our data to two sureddits: Apple & iPhone. Specifically, our project contains three stages: (1) explore the online dynamics through topic modeling, i.e.,   extract the underlying themes/topics sourrounding iPhone to see the longitudinal change; (2) with 3380 posts sampled for manual labeling, we trained various classification model and apply the best model to predict the sentiment (negative, neutral, positive) for remaining comment posts; (3) use monthly discussion volume (i.e., number of comments posted), the underlying topics as well aggregated sentiment strengh obtained in the first two steps, together with some external factors (e.g., GDP) to explore how social media would reflect or correlate with real-word business metrics (e.g., iPhone sales).

### Data Access Statement
- The raw data from clickhouse:  https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments  
- Cleaned data (the data used in our project): https://drive.google.com/drive/folders/10toX4JXv3NHkC5owntA7LWuxKkyROyIe?usp=sharing
- Labeled data for sentiment analysis (can also be accessed in this Repository):  https://drive.google.com/drive/folders/1-ybm8bWPhP7-qCwKiNedACQkUJA2WbLN?usp=sharing 
- Results for sentiment classification: https://drive.google.com/drive/folders/1-ybm8bWPhP7-qCwKiNedACQkUJA2WbLN?usp=sharing  

### Codes Execution 
Please follow the below steps to run the codes for each stages:

1. Topic Modeling: run the " " file.
2.  Sentiment Analysis: set up the environment by installing all packages listed in "2. requirements.txt" file, then run the "2. Sentiment classification.ipynb" file with the input data from the 'Labeled" folder (for model training and evaluation, uploaded in this repository) and  "Data" folder (for unlabeled data's sentiment prediction, not uploaded here due to the limited repository storage).
3.  Offline Sales Prediction: run the " " file.

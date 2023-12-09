# MADS699 Capstone: Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

## Project Overview  
We use the Reddit Comments Dataset between 2008 and 2019, a publicly available data set from Clickhouse, to gauge the online opinion dynamics about the iPhone and explore to what extent social media metrics could reflect real-world behavior patterns. We collected the data from Clickhouse and kept iPhone-related posts from two subreddits: Apple & iPhone. Then we proceed to the following stage of analysis step by step: (1)  extract the underlying themes/topics surrounding iPhone over the years with various topic modeling techniques; (2) sample 3380 posts randomly for manual labeling (negative, neutral, positive) and trained various sentiment classification models with various types of features, we then apply the best model to predict the sentiment of all remaining unlabeled posts; (3) use monthly discussion volume (i.e., number of comment posts),  topic prevalence as well as the sentiment strength in each comment post obtained in the first two steps, together with some external factors (e.g., price, GDP) to analyze the impact on real-word iPhone sales, trying to find any correlation.

## Data Access Statement

Starting from the [Reddit Comments Dataset](https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments) from clickhouse, we screened the irrelevant posts for this project. 
- **Data**: this folder contains all iPhone-related comment data from two subreddits (iphone & apple) during 2008 and 2019. Due to the storage limitation of this Repo, please check [this folder](https://drive.google.com/drive/folders/10toX4JXv3NHkC5owntA7LWuxKkyROyIe?usp=sharing) to access it. 
- **Labeled_sentiment classification**: this folder contains 3380 data randomly sampled for human labeling, which was used for sentiment classification. It can be accessed in this Repo directly.    
- **Results_sentiment classification**: this folder contains the results returned by the sentiment classification (step 2), in which the best classification model was found and applied to predict the sentiment embedded in each unlabeled posts from the **Data** folder. Two additional columns were added when applying the best model for sentiment prediction: (1) *sentiment label*: 1 means positive sentiment, 0 means neutral, -1 means negative sentiment; (2) *type*: "labeled" vs. "predicted", indicating whether the sentiment label was labeled by human coders or predicted by the best model.   Due to the storage limitation of this Repo, please access it in [this folder](https://drive.google.com/drive/folders/1-ybm8bWPhP7-qCwKiNedACQkUJA2WbLN?usp=sharing).   

## Codes Execution 
Please follow the below steps to run the codes for each stage:

1. **Topic Modeling**: run the " " file.
2. **Sentiment Classification**: install the packages listed in the ***part2_requirements.txt*** file, then run the ***part2_sentiment classification.ipynb*** file with input data including the labeled data from the ***Labeled_sentiment classification*** folder for model training & evaluation, as well as the ***Data*** folder for sentiment prediction of all unlabeled data.   The ouput, which contains all cleaned data with the sentiment labels either labeled by human coders or predicted by the best classification model,  was saved in the ***Results_sentiment classification*** folder. Please check **Data Access Statement** section for details about those data folders.   
3. **Impact on real-world metrics**: run the " " file.

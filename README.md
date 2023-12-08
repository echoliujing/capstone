# MADS699 Capstone: Prediction of Real-word iPhone Sales with Opinion Dynamics on Reddit

## Project Overview  
We use the Reddit Comment Data between 2008 and 2019, a publicly available data set from clickhouse, to gauge the online opinion dynamics about iPhone and explore to what extent would social media metrics could reflect real-world behaviour patterns. We collected the data from clickhouse and keep iPhone-related posts from two sureddits: Apple & iPhone. Then we proceed the follow stage of analysis step by step: (1)  extract the underlying themes/topics sourrounding iPhone along the years with variou topic modeling techniquess; (2) sample 3380 posts randomly for manual labeling (negative, neutral, positive) and trained various sentiment classification models with various types of features, we then apply the best model to predict the sentiment of all remaining unlabeled posts; (3) use monthly discussion volume (i.e., number of comments posts),  topic prevalence as well as the sentiment strengh for each comment post obtained in the first two stages, together with some external factors (e.g., price, GDP) to predict real-word iPhone sales.

## Data Access Statement
- **The raw data**: this is the raw reddit comments data set from clickhouse, and it can be accessed via [this link](https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments).  
- **The data**: this is the cleaned data which contains iPhone-related comment posts from two subreddits (iphone & apple). Please check [this folder](https://drive.google.com/drive/folders/10toX4JXv3NHkC5owntA7LWuxKkyROyIe?usp=sharing) to access it. 
- **Labeled data for stage 2**: this folder contains the data randomly sampled for human labeling and was used for sentiment classification. It can be accessed in the ***Labled_sentiment classification*** folder in this Repo.    
- **Predicted data from stage 2**:  this folder contains all cleaned data with two additional columns added in stage 2: (1) *sentiment label*: 1 means positive sentiment, 0 means neutral, -1 means negative sentiment; (2) *type*: "labeled" vs. "predicted", indicating whether the sentiment label was labeled by the the two human coders or predicted by the best model found in the sentiment classification stage. Due to the storage limitation of this Repo, they are accessed in [this folder](https://drive.google.com/drive/folders/1-ybm8bWPhP7-qCwKiNedACQkUJA2WbLN?usp=sharing).  

## Codes Execution 
Please follow the below steps to run the codes for each stage:

1. **Topic Modeling**: run the " " file.
   
2. **Sentiment Classification**: set up the environment by installing all packages listed in the ***2. requirements.txt*** file, then run the ***2. Sentiment classification.ipynb*** file with input data include the labeled data (i.e., the ***Labeled_sentiment classification*** folder) for model training & evaluation, as well as the cleaned data for sentiment prediction of all unlabeled data (i.e., the ***The Data** folder).   The final data with sentiment labels either manually labeled or predicted by the best model found in stage 2 can be accessed in the ***Predicted data from stage 2*** folder, and the best models found in this process can be accessed in the ***Models_sentiment classification*** folder in ths Repo. Please check *Data Access Statement* section for details about the data folders.

3. **Offline Sales Prediction**: run the " " file.

# MADS699 Capstone: Prediction of Real-world iPhone Sales with Opinion Dynamics on Reddit

## Project Overview  
We use the Reddit Comments Dataset between 2008 and 2019, a publicly available data set from Clickhouse, to gauge the online opinion dynamics about the iPhone and explore to what extent social media metrics could reflect real-world behavior patterns. We collected the data from Clickhouse and kept iPhone-related posts from two subreddits: Apple & iPhone. Then we proceed to the following stage of analysis step by step: (1)  extract the underlying themes/topics surrounding iPhone over the years with various topic modeling techniques; (2) sample 3380 posts randomly for manual labeling (negative, neutral, positive) and trained various sentiment classification models with various types of features, we then apply the best model to predict the sentiment of all remaining unlabeled posts; (3) use monthly discussion volume (i.e., number of comment posts),  topic prevalence as well as the sentiment strength in each comment post obtained in the first two steps, together with some external factors (e.g., price, GDP) to analyze the impact on real-word iPhone sales, trying to find any correlation.

## Data Access Statement

Starting from the [Reddit Comments Dataset](https://clickhouse.com/docs/en/getting-started/example-datasets/reddit-comments) from clickhouse, we screened the irrelevant posts for this project. 
- **data**: this folder contains the input (i.e., raw Reddit data) and output data (i.e., iPhone-related comment data from two subreddits) during 2008 and 2019. Due to the storage limitation of this Repo, please check [this link](https://drive.google.com/drive/folders/10toX4JXv3NHkC5owntA7LWuxKkyROyIe?usp=sharing) to access it.
- **results_topic modeling**: this folder contains the results returned by the part 1(topic modeling): the aggregated document data (.csv file), the doc_topic matrix (.pkl), as well as the summarized 8 topic categories matched to individual topics across the years (.csv file).  Due to the storage limitation of this Repo, please find them via [this link](https://drive.google.com/drive/folders/1DoUdMhHIEPUzIRiMj4dj8P7KkmHIIB_v?usp=sharing). 
- **labeled_sentiment classification**: this folder contains the labeled data used for part 2(sentiment classification). It can be accessed in this Repo directly.    
- **results_sentiment classification**: this folder contains the results returned by part 2 (sentiment classification): (1) the best models found in the RandomizedSearchCV process;  and (2) all Reddit data with sentiment labels predicted by the best model.   Compared with **Data** foder, two additional columns were added : (1) *sentiment label*: 1 means positive sentiment, 0 means neutral, -1 means negative sentiment; (2) *type*: "labeled" vs. "predicted", indicating whether the sentiment label was labeled by human coders or predicted by the best model.   Due to the storage limitation of this Repo, please access it in [this link](https://drive.google.com/drive/folders/1-ybm8bWPhP7-qCwKiNedACQkUJA2WbLN?usp=sharing).   

## Codes Execution 
Please follow the below steps to run the codes for each stage:

0. **Data collection and processing**: rune the **part0_data_cleaning.ipynb** file. Both the input and output data were saved in the **data** folder. 
1. **Topic Modeling**: run the **part1_lda.ipynb** file. The input data is from the **data** folder and the ouput were saved in the **results_topic modeling** folder. 
2. **Sentiment Classification**: run the ***part2_sentiment classification.ipynb*** file. The input includes the labeled data from the ***labeled_sentiment classification*** folder for model training & evaluation, and the iPhone-related Reddit data from the ***data*** folder for sentiment prediction.   The ouput (i.e.,  cleaned Reddit data with sentiment labels) were saved in the ***results_sentiment classification*** folder.  
3. **Impact on real-world metrics**: run the ***part3_real-world impact.ipynb*** file with the input data from results from Part 1 and Part 2 in Google Drive. And integrated with some real-world data including iPhone sales by month, American regions ratio, and GDP growth rate. These data mostly are from 3rd party institution "Statistia", and these data are directly written with variables in the notebook. The first data integration steps of topic modeling and sentiment result, as well as applying comparison sentiment to posts level are very time costly even with Colab, maybe Colab Pro or using the cloud CPU of Google will fasten the process but have not been tested yet.

*Please check **Data Access Statement** section for details about those data folders.*  

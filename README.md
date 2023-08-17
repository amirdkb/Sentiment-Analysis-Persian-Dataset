# Sentiment-Analysis-Persian-Dataset
### Persian Sentiment Analysis for Neshan Dataset
Perform sentiment analysis on Persian user comments about specific locations using Neshan dataset.
### Description
This project focuses on sentiment analysis of user comments in Persian language related to specific locations, utilizing a dataset from the Neshan app. By analyzing the sentiments expressed in these comments, we can gain insights into how users perceive and react to different places.

### Dependencies
install necessary libraries using following command 
```
pip install pandas scikit-learn hazm
```
### Dataset 
This sentiment analysis project utilizes two datasets: train.csv and test.csv. These datasets are crucial components for training and evaluating our sentiment analysis model on Persian text data.the `test.csv` contains sentences without labels and we are going to predict their labels and save them in another file with name `test_with_label.csv`.<br>

`train.csv`<br>
The train.csv dataset is designed for training our sentiment analysis model. It contains a collection of text samples in Persian, paired with corresponding sentiment labels.<br>
`test.csv`<br>
The test.csv dataset is used to evaluate the performance of our trained sentiment analysis model. Similar to train.csv, it contains text samples in Persian, but it does not include sentiment labels.<br>
`test_with_label.csv`<br>
This file is result file after execution, it is test data with predicted labels. 
### Implementation 
We utilized a Linear Support Vector Machine (SVM) model for analyzing this dataset. The model was trained and evaluated using the training data to gauge its effectiveness. Subsequently, the trained model was saved with name `trained_model.pkl`. This saved model can be effectively employed to predict labels for new samples.
### Results
Using `Predict` function you can use predict label of a new sample :
```
sentence ='فروختن ماشین سرقتی به مردم ، ۶ ماه پیش ماشین خریدم  از این نمایشگاه ایست بازرسی جلومو گرفتن ماشینو بردن پارکینگ خودمم بازداشت شدم تا بفهمونم از این نمایشگاه خریدم دوروز نگه داشتن بعد معلوم شد ماشین سرقتی بوده خودشون شماره شاسی کوبیدن پلاک درست کردن فروختن'
predict(sentence)
```
**Result:**
```
array(['Negative'], dtype='<U8')
```
**Model Evaluation Metrics:**

|         | Precision | Recall | F1-Score | Support |
|---------|-----------|--------|----------|---------|
| Negative|   0.83    |  0.83  |   0.83   |   248   |
| Neutral |   0.57    |  0.51  |   0.54   |    72   |
| Positive|   0.82    |  0.85  |   0.83   |   189   |
|---------|-----------|--------|----------|---------|
| Accuracy|           |        |   0.79   |   509   |
|Macro avg|   0.74    |  0.73  |   0.74   |   509   |
|Weighted avg|0.79    |  0.79  |   0.79   |   509   |



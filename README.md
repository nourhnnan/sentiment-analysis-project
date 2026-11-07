Customer Review Sentiment Analyzer

Binary sentiment classification (positive/negative) of Amazon customer reviews.

Dataset
Amazon Reviews for Sentiment Analysis (binary) from Kaggle:
https://www.kaggle.com/datasets/yacharki/amazon-reviews-for-sa-binary-negative-positive-csv

The training file has about 3.6 million reviews, so I worked on a random
3% sample (108,000 reviews, random_state=42).
Steps
1. Download the data from Kaggle in Google Colab
2. Take a random sample, keeping the classes balanced (about 50/50)
3. Clean the text (title + review, lowercase, remove symbols)
4. Split into train/test (80/20, stratified)
5. TF-IDF (50,000 features, fit on the training set only) + Logistic Regression

Result
Test accuracy: 0.8956

How to run
Open sentimentProject.ipynb in Google Colab and run all cells.

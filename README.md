Customer Review Sentiment Analyzer

 The notebook classifies Amazon reviews as negative(0) or positive(1) with three classic models: Logistic Regression,Naive Bayes and a linear SVM. Reviews are turned into numbers with BM25 weights.

The dataset is [Amazon Reviews for SA binary (negative/positive) CSV](https://www.kaggle.com/datasets/yacharki/amazon-reviews-for-sa-binary-negative-positive-csv) on Kaggle.

 Notebook:

sentimentProject_final.ipynb holds all the code and its output. It runs in Google Colab

What the notebook does

1. Takes a random 3% sample of the Kaggle training file (108,000 reviews, random_state=42).
2. Merges each review's title and text, lowercases it and strips HTML tags, links and symbols.
3. Splits the sample 80/20 into 86,400 training and 21,600 test reviews, stratified by label.
4. Builds BM25 features from the 50,000 most frequent words, with k1 = 1.5 and b = 0.75. The vocabulary, idf and average review length come from the training reviews only.
5. Trains the three models with their default settings and compares them on the test set.
6. Takes each model to an underfit, a good fit and an overfit version by changing one setting: C for Logistic Regression and the SVM, alpha for Naive Bayes.


Limitations

- The models were trained on 3% of the training file.
- k1 and b were fixed at common values and not tuned.
- BM25 counts words and ignores their order, so negation is often misread.
- The data is in English only.

Kaggle (https://kaggle.com/datasets/yacharki/amazon-reviews-for-sa-binary-negative-positive-csv)
🛒 Amazon Reviews for Senti-Analysis Binary -N/P+
Containes train.csv + test.csv + readme.csv

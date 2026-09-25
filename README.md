Sentiment Analysis of Online Hotel Reviews

Project Overview

This repository contains the code and supporting materials for the dissertation “A Comparative Analysis of Machine Learning Algorithms for Sentiment Analysis of Online Hotel Reviews.”

The project investigates sentiment classification of online hotel reviews using traditional machine-learning methods, a BiLSTM neural network with additive attention, and a transformer-based benchmark.

Dataset

The study uses the 515K Hotel Reviews Data in Europe dataset from Kaggle.

- Original records: 515,738
- Records after cleaning and duplicate removal: 503,433
- Main experimental sample: 50,000 reviews
- Positive reviews: 41,485 (82.97%)
- Negative reviews: 8,515 (17.03%)

Sentiment labels are created from the reviewer score:

- Positive: Reviewer Score ≥ 7.0
- Negative: Reviewer Score < 7.0

Models

The repository covers the following approaches:

1. Logistic Regression with TF-IDF
2. Multinomial Naive Bayes with TF-IDF
3. Random Forest with TF-IDF
4. BiLSTM with additive attention
5. Transformer-based sentiment benchmark using "cardiffnlp/twitter-roberta-base-sentiment-latest"

Methodology

The main workflow includes:

- Data cleaning and quality checking
- Duplicate removal
- Combining positive and negative review fields
- Sentiment-label construction
- Text preprocessing
- TF-IDF feature extraction using unigrams and bigrams
- Train-test splitting
- Model training
- Hyperparameter tuning
- Five-fold stratified cross-validation
- Model evaluation
- BiLSTM and attention-based modelling
- Optional transformer benchmarking

A fixed random state of 42 is used to support reproducibility.

Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Because the dataset contains substantially more positive than negative reviews, multiple evaluation metrics are considered rather than relying only on accuracy.



Reproducibility

The experiments use a consistent dataset preparation and modelling workflow. Important settings such as the dataset source, sampling procedure, sentiment-label definition, preprocessing, model configuration, hyperparameters and evaluation metrics are documented in the dissertation.

Important Note

The transformer component is treated as an optional benchmark. Transformer results should only be reported when the corresponding experiment has actually been executed. This repository therefore distinguishes between implemented methodology and verified experimental results.

Dataset Source

Kaggle: 515K Hotel Reviews Data in Europe

https://www.kaggle.com/datasets/jiashenliu/515k-hotel-reviews-data-in-europe

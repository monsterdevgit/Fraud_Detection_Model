# Fraud Detection Model

This project implements a fraud detection model using various machine learning techniques. The primary focus is on identifying fraudulent transactions in credit card data.

## Table of Contents

- Introduction
- Dependencies
- Dataset
- Exploratory Data Analysis (EDA)
- Model Building
- Use Cases
- Evaluation Metrics
- Citations

## Introduction

Fraud detection is a critical task in the financial industry. This project utilizes a dataset of credit card transactions to build a predictive model that can distinguish between legitimate and fraudulent transactions.

## Dependencies

The following libraries are required to run the project:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`

You can install the required libraries using pip:

```bash
pip install numpy pandas matplotlib scikit-learn
```

## Dataset

The dataset used in this project is [`creditcard.csv`](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download), which contains transactions made by credit cards in September 2013 by European cardholders.

### Overview
The dataset consists of transactions that occurred over two days, with a total of 284,807 transactions, of which 492 are fraudulent. The positive class (frauds) accounts for only 0.172% of all transactions, making the dataset highly unbalanced.

### Features
The dataset includes only numerical input variables, which are the result of PCA (Principal Component Analysis) transformation. Unfortunately, due to confidentiality issues, the original features and more background information cannot be provided.
- Features `V1` to `V28` are the principal components obtained through PCA.
- The features `Time` and `Amount` have not been transformed:
  - **Time**: Seconds elapsed between each transaction and the first transaction in the dataset.
  - **Amount**: The transaction amount, which can be used for example-dependent cost-sensitive learning.
- **Class**: The response variable that indicates whether a transaction is fraudulent (1) or not (0).

## Exploratory Data Analysis (EDA)
The initial analysis of the dataset includes:
- Checking for missing values
- Statistical summary of the features
- Visualizations of transaction amounts and class distributions

## Model Building
The following machine learning algorithms are implemented:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

Model training involves splitting the dataset into training and test sets, followed by fitting the models and making predictions.

## Use Cases
Fraud detection models can be applied in various scenarios, including:
- **Credit Card Transactions**: Identifying fraudulent charges to protect consumers and banks.
- **Insurance Claims**: Detecting false claims to reduce losses for insurance companies.
- **E-commerce Transactions**: Preventing fraudulent purchases and chargebacks in online retail.
- **Telecommunications**: Identifying fraudulent activities in mobile phone usage, such as SIM card cloning.
- **Financial Services**: Monitoring and detecting unauthorized access or transactions in banking applications.

## Evaluation Metrics
The performance of the models is evaluated using:
- Accuracy Score
- F1 Score
- Precision Score
- Recall Score
- ROC AUC Score

Confusion matrices are also generated to visualize the performance of the models.

## Citations

Please cite the following works for further reading and acknowledgment:

1. Andrea Dal Pozzolo, Olivier Caelen, Reid A. Johnson, and Gianluca Bontempi. *Calibrating Probability with Undersampling for Unbalanced Classification*. In Symposium on Computational Intelligence and Data Mining (CIDM), IEEE, 2015.

2. Dal Pozzolo, Andrea; Caelen, Olivier; Le Borgne, Yann-Ael; Waterschoot, Serge; Bontempi, Gianluca. *Learned lessons in credit card fraud detection from a practitioner perspective*, Expert Systems with Applications, 41(10), 4915-4928, 2014, Pergamon.

3. Dal Pozzolo, Andrea; Boracchi, Giacomo; Caelen, Olivier; Alippi, Cesare; Bontempi, Gianluca. *Credit card fraud detection: a realistic modeling and a novel learning strategy*, IEEE Transactions on Neural Networks and Learning Systems, 29(8), 3784-3797, 2018, IEEE.

4. Dal Pozzolo, Andrea. *Adaptive Machine learning for credit card fraud detection*, ULB MLG PhD thesis (supervised by G. Bontempi).

5. Carcillo, Fabrizio; Dal Pozzolo, Andrea; Le Borgne, Yann-Aël; Caelen, Olivier; Mazzer, Yannis; Bontempi, Gianluca. *Scarff: a scalable framework for streaming credit card fraud detection with Spark*, Information Fusion, 41, 182-194, 2018, Elsevier.

6. Carcillo, Fabrizio; Le Borgne, Yann-Aël; Caelen, Olivier; Bontempi, Gianluca. *Streaming active learning strategies for real-life credit card fraud detection: assessment and visualization*, International Journal of Data Science and Analytics, 5(4), 285-300, 2018, Springer International Publishing.

7. Bertrand Lebichot, Yann-Aël Le Borgne, Liyun He, Frederic Oblé, Gianluca Bontempi. *Deep-Learning Domain Adaptation Techniques for Credit Cards Fraud Detection*, INNSBDDL 2019: Recent Advances in Big Data and Deep Learning, pp 78-88, 2019.

8. Fabrizio Carcillo, Yann-Aël Le Borgne, Olivier Caelen, Frederic Oblé, Gianluca Bontempi. *Combining Unsupervised and Supervised Learning in Credit Card Fraud Detection*, Information Sciences, 2019.

9. Yann-Aël Le Borgne, Gianluca Bontempi. *Reproducible Machine Learning for Credit Card Fraud Detection - Practical Handbook*.

10. Bertrand Lebichot, Gianmarco Paldino, Wissam Siblini, Liyun He, Frederic Oblé, Gianluca Bontempi. *Incremental learning strategies for credit cards fraud detection*, International Journal of Data Science and Analytics.

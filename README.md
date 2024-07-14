## Credit-Card-Fraud-Detection

This project aims to predict fraudulent credit card transactions using machine learning models. We'll analyze customer-level data from a research collaboration between Worldline and the Machine Learning Group [University Libre de Bruxelles](https://www.ulb.ac.be/).

### Problem Statement

The dataset, available on [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud), contains 284,807 transactions (September 2013, Europe) with only 492 marked as fraudulent. This significant imbalance requires special attention during model building.

### Business Problem Overview

For banks, retaining customers is paramount. Banking fraud, however, jeopardizes this goal by causing financial losses and damaging trust. The Nilson report estimates that banking frauds would reach $30 billion globally by 2020. As digital payments rise, so do fraudulent activities. Machine learning offers a powerful weapon for fraud detection, enabling proactive monitoring and prevention. It helps banks reduce manual review time, minimize chargebacks and fees, and avoid denying legitimate transactions.

### Understanding and Defining Fraud

Credit card fraud involves any unauthorized use of a cardholder's information for financial gain. Skimming, the most common method, duplicates magnetic strip data. Other forms of fraud include:

* Manipulation/alteration of genuine cards
* Creation of counterfeit cards
* Stolen/lost credit card use
* Fraudulent telemarketing

### Data Dictionary

The dataset contains credit card transactions made by European cardholders over two days in September 2013. With 492 fraudulent transactions out of 284,807, the data is highly imbalanced (positive class: 0.172%). Principal Component Analysis (PCA) has been applied to features (V1, V2, ..., V28) to preserve confidentiality. Only features 'time' (seconds elapsed from the first transaction) and 'amount' remain in their original form. The 'class' feature indicates fraud (1) or not (0).

### Project Pipeline

The project follows these four steps:

1. **Data Understanding:** Load and explore the data to identify relevant features for model building.
2. **Exploratory Data Analysis (EDA):** Perform univariate and bivariate analyses to understand data distribution and relationships. Feature transformations might be necessary, but due to Gaussian variables, Z-scaling may not be required. However, address any skewness to avoid issues during model building.
3. **Train/Test Split:** Split the data for training and testing to evaluate model performance on unseen data. K-fold cross-validation is recommended for balanced representation of the minority class in test folds. Choose an appropriate k value.
4. **Model Building/Hyperparameter Tuning:** Experiment with different models and fine-tune their hyperparameters to achieve optimal performance. Explore various sampling techniques to potentially improve model results.
5. **Model Evaluation:** Evaluate models using appropriate metrics considering the imbalanced data. Since identifying fraudulent transactions is more crucial, choose metrics that reflect this business goal.

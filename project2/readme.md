# Fraud Detection Using Machine Learning

## Project Overview

This project focuses on building a machine learning pipeline to detect fraudulent financial transactions using the PaySim dataset. Fraud detection is an important application of data science in the banking and financial sector, helping organizations identify suspicious activities and minimize financial losses.

The PaySim dataset simulates mobile money transactions and contains both legitimate and fraudulent transactions. Since fraudulent transactions represent only a very small percentage of the total transactions, the dataset is highly imbalanced. This project addresses the imbalance problem using the SMOTE (Synthetic Minority Over-sampling Technique) algorithm.

Two supervised machine learning algorithms, Logistic Regression and Random Forest, were trained and evaluated to determine their effectiveness in identifying fraudulent transactions.

## Objectives

* To analyze and preprocess transaction data.
* To understand the distribution of fraudulent and non-fraudulent transactions.
* To handle class imbalance using SMOTE.
* To build classification models using Logistic Regression and Random Forest.
* To evaluate model performance using Precision, Recall, and ROC-AUC instead of relying solely on Accuracy.
* To identify the most important features contributing to fraud detection.

## Dataset

The project uses the PaySim Fraud Detection Dataset, which is a synthetic mobile money transaction dataset designed to reflect real-world financial transaction patterns.

### Important Features

* **step:** Represents the time step of the transaction.
* **type:** Type of transaction (CASH_IN, CASH_OUT, DEBIT, PAYMENT, TRANSFER).
* **amount:** Amount involved in the transaction.
* **oldbalanceOrg:** Sender's account balance before the transaction.
* **newbalanceOrig:** Sender's account balance after the transaction.
* **oldbalanceDest:** Receiver's account balance before the transaction.
* **newbalanceDest:** Receiver's account balance after the transaction.
* **isFraud:** Target variable indicating whether the transaction is fraudulent (1) or legitimate (0).

## Methodology

The following steps were performed during the project:

1. Loaded and explored the dataset.
2. Checked for missing values and data consistency.
3. Visualized the fraud distribution to understand class imbalance.
4. Removed unnecessary identifier columns.
5. Created additional features using balance differences.
6. Encoded categorical transaction types into numerical values.
7. Split the dataset into training and testing sets.
8. Applied SMOTE to balance the training data.
9. Trained Logistic Regression and Random Forest models.
10. Evaluated both models using Precision, Recall, Classification Report, Confusion Matrix, and ROC-AUC score.
11. Compared the performance of the models.
12. Analyzed feature importance using Random Forest.

## Evaluation Metrics

Traditional accuracy can be misleading when dealing with highly imbalanced datasets. Therefore, the following metrics were used:

* **Precision:** Measures how many transactions predicted as fraud were actually fraudulent.
* **Recall:** Measures how many actual fraud cases were successfully detected.
* **ROC-AUC:** Evaluates the model's ability to distinguish between fraudulent and non-fraudulent transactions.
* **Confusion Matrix:** Provides a detailed breakdown of correct and incorrect predictions.

## Results

Both Logistic Regression and Random Forest were capable of identifying fraudulent transactions. However, Random Forest generally achieved better fraud detection performance due to its ability to capture complex relationships within the data.

The comparison of evaluation metrics demonstrated the importance of prioritizing fraud detection effectiveness over simple accuracy measures.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn (SMOTE)
* Visual Studio Code

## Conclusion

This project demonstrates the practical application of supervised machine learning techniques in fraud detection. By addressing class imbalance through SMOTE and evaluating models using appropriate metrics, it is possible to build robust systems capable of detecting fraudulent financial activities.

The knowledge gained from this project provides valuable experience in data preprocessing, handling imbalanced datasets, model training, and performance evaluation, all of which are essential skills for aspiring data scientists and machine learning practitioners.

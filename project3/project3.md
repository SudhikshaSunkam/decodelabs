# Customer Segmentation using PCA and K-Means

## Project Overview

This project performs Customer Segmentation using Unsupervised Machine Learning techniques.

The objective is to discover hidden customer groups from retail transaction data without using predefined labels.

## Dataset

Online Retail Dataset (UCI Repository)

Source:
https://archive.ics.uci.edu/ml/datasets/online+retail

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn

## Machine Learning Techniques

1. Data Cleaning
2. Feature Engineering
3. Standardization
4. Principal Component Analysis (PCA)
5. K-Means Clustering
6. Elbow Method
7. Silhouette Score Evaluation

## Workflow

- Load retail transaction data
- Clean missing and invalid records
- Create customer-level features
- Standardize numerical features
- Apply PCA for dimensionality reduction
- Determine optimal clusters using Elbow Method
- Validate clusters using Silhouette Score
- Perform customer segmentation
- Generate business personas

## Results

The model successfully grouped customers into distinct segments based on purchasing behavior.

These customer segments can help businesses:

- Improve marketing campaigns
- Personalize offers
- Increase customer retention
- Improve business decision-making

## Future Improvements

- 3D PCA Visualization
- DBSCAN Clustering
- Hierarchical Clustering
- Interactive Dashboard using Streamlit

Business Personas

Cluster 0 – Premium Customers

Highest spending
Frequent purchases
High quantity ordered

Cluster 1 – Regular Customers

Medium spending
Consistent purchasing

Cluster 2 – Occasional Buyers

Purchase rarely
Low quantity

Cluster 3 – New/Low Value Customers

Lowest spending
Target with promotions
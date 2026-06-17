# Task 1: Data Collection & Dataset Understanding

## Project Title

**Online Store Sales Analysis and Revenue Prediction**

---

## 1. Project Objective

The objective of this project is to analyze online store order data to understand customer purchasing behavior, sales trends, payment preferences, and order outcomes. The dataset will also be used to build a predictive model for estimating order revenue.

---

## 2. Dataset Information

### Dataset Name

Online Store Orders Dataset

### Source

Dataset provided by the internship organization.

---

## 3. Feature Description

| Column Name     | Description                        | Data Type   |
| --------------- | ---------------------------------- | ----------- |
| OrderID         | Unique order identifier            | Integer     |
| Date            | Date of order                      | Date        |
| CustomerID      | Unique customer identifier         | Integer     |
| Product         | Product purchased                  | Categorical |
| Quantity        | Number of units ordered            | Integer     |
| UnitPrice       | Price per unit                     | Numeric     |
| ShippingAddress | Delivery location                  | Categorical |
| PaymentMethod   | Method used for payment            | Categorical |
| OrderStatus     | Current order status               | Categorical |
| TrackingNumber  | Shipment tracking number           | Categorical |
| ItemsInCart     | Number of items in shopping cart   | Integer     |
| CouponCode      | Applied discount coupon            | Categorical |
| ReferralSource  | Source from which customer arrived | Categorical |
| TotalPrice      | Final order value                  | Numeric     |

---


## 4. Initial Findings

### Dataset Dimensions

```text
Rows: 1200
Columns: 14
```

### Missing Values

The CouponCode column contains missing values, indicating that not all customers used discount coupons during purchase.

### Data Types Summary

| Type        | Count |
| ----------- | ----- |
| Numerical   | 4     |
| Categorical | 7     |
| Date        | 1     |
| Identifier  | 2     |

---

## 5. Conclusion

The Online Store Orders dataset contains customer purchase information and sales-related attributes. It includes numerical, categorical, and date-based features that make it suitable for data cleaning, exploratory data analysis, visualization, and predictive modeling. Initial exploration indicates the presence of missing values that will be addressed during the data preprocessing stage in Task 2.

# Task 2: Data Cleaning & Preprocessing

## 1. Objective

The purpose of this phase was to prepare the dataset for analysis by handling missing values, checking duplicates, validating data types, and creating additional features.


## 2. Missing Values

The CouponCode column contained missing values. These missing entries were replaced with "No Coupon" because they indicate orders where no discount coupon was applied.

## 3. Duplicate Records

The dataset was checked for duplicate records. Any duplicate rows were removed to maintain data integrity.

## 4. Data Type Conversion

The Date column was converted into datetime format to facilitate time-based analysis.

## 5. Feature Engineering

Three new features were created:

- Month
- Year
- DayName

These features will help analyze seasonal and temporal sales trends.


## 6. Conclusion

The dataset was successfully cleaned and prepared for exploratory data analysis and predictive modeling.

# Task 3: Exploratory Data Analysis

## 1. Objectives

The purpose of EDA is to discover trends, patterns, and business insights from the Online Store Orders dataset.

## 2. Analyses Performed

1. Product-wise Revenue Analysis
2. Payment Method Analysis
3. Order Status Distribution
4. Referral Source Performance
5. Monthly Sales Trend Analysis
6. Coupon Usage Analysis

## 3. Key Findings

### Overall Conclusion from EDA

The exploratory analysis revealed that product demand, payment preferences, marketing channels, seasonality, and promotional strategies all have a measurable impact on sales performance. Chairs emerged as the top revenue-generating product, online payments were the dominant transaction method, Instagram was the most effective customer acquisition channel, June recorded the highest sales, and the FREESHIP coupon delivered the strongest promotional performance. However, the high proportion of cancelled orders highlights an operational area that requires further investigation and improvement.

## 4. Conclusion

The EDA phase revealed important customer purchasing patterns, sales trends, and operational insights that can support business decision-making and predictive modeling.

# Task 4: Data Visualization

## 1. Objective

The objective of this phase was to visually explore sales patterns, customer behavior, marketing performance, and promotional effectiveness using charts and graphs.

## 2. Visualizations Created

1. Revenue by Product
2. Payment Method Usage
3. Order Status Distribution
4. Revenue by Referral Source
5. Monthly Sales Trend
6. Revenue by Coupon Code

## 3. Major Findings

- Chair was the highest revenue-generating product.
- Online payment was the most frequently used payment method.
- Cancelled orders represented the largest order status category.
- Instagram generated the highest revenue among referral sources.
- June recorded the highest monthly sales.
- FREESHIP was the most successful coupon code.

## 4. Conclusion

The visual analysis highlighted important business trends related to customer purchasing behavior, payment preferences, marketing effectiveness, seasonal demand, and promotional strategies. These insights can support data-driven business decisions and guide future predictive modeling efforts.

# Task 5: Predictive Modeling

## 1. Objective

The objective of this phase was to build a machine learning model capable of predicting the total order value based on product, payment, marketing, and customer order information.

## 2. Model Used

1. Linear Regression
2. Random Forest Regressor

## 3. Data Preparation

- Removed identifier columns.
- Converted categorical variables using one-hot encoding.
- Split data into training and testing sets.

## 4. Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score

## 5. Results

| Model                   | R² Score |
| ----------------------- | -------- |
| Linear Regression       | 0.8313   |
| Random Forest Regressor | 0.9997   |


## Conclusion

The Random Forest Regressor significantly outperformed Linear Regression. While Linear Regression explained 83.13% of the variation in order revenue, Random Forest achieved an R² score of 99.97%, indicating near-perfect prediction performance. Therefore, Random Forest was selected as the final model for revenue prediction.
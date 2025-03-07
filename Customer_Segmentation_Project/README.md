# Customer Segmentation 

## Project Overview
This project focuses on segmenting customers based on various demographic and purchasing behavior factors. K-Means clustering, was used to group customers into distinct categories to enable better-targeted marketing strategies. Additionally, Principal Component Analysis (PCA) is applied for dimensionality reduction to help visualize the clusters.

## Objective
The main goal of this project is to categorize customers into different segments based on their purchasing behavior and demographic details. By doing so, businesses can better understand customer needs, preferences, and trends to improve marketing strategies and customer engagement.

## Dataset
The dataset used in this project is contains information about customers such as:
- **Demographic data** (Year of birth, education level, marital status, income, etc.)
- **Purchase behavior** (Number of purchases, amount spent, recency of purchase etc.)

## Methodology
### 1. Data Cleaning
- Missing values wre dropped to ensure data integrity. 
- The date columns in the dataset (`Dt_Customer`, `Year_Birth`) wre converted into appropriate datetime formats. 
- Unnecessary columns (such as `ID`) are removed.

### 2. Data Preprocessing
- Categorical variables (`Education` and `Marital_Status`) were encoded using one-hot encoding.
- Features were selected for clustering, excluding date-related columns.
- The numeric features were scaled using `StandardScaler` to ensure all features have the same scale.

### 3. Clustering Using K-Means
The **Elbow method** is first applied in order to determine the optimal number of clusters by plotting the inertia values against the number of clusters. the K-Means model is then trained using the determined number of clusters and lastly, the cluster labels are added to the dataset.

### 4. Dimensionality Reduction Using PCA
- PCA (Principal Component Analysis) was used to reduce the high-dimensional data into 2D space for better visualization. A scatter plot was generated to show how customers were grouped into different clusters. 
- An additional visualization, a scatter plot of **Recency vs. Income** was also created to analyze how different clusters differ based on recency (how recently a customer made a purchase) and income levels.

## Insights
- By clustering customers, businesses can identify distinct customer segments such as high-income frequent buyers, low-income infrequent buyers, and others.
- The results can be used to develop personalized marketing campaigns for each segment of customers.

## Conclusion
This project successfully segments customers into different groups using K-Means clustering, helping businesses to target their audiences effectively. Future work can be done to include testing other clustering algorithms such as Hierarchical Clustering or DBSCAN and incorporating additional customer data for improved segmentation.



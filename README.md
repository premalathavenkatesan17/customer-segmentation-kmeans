# Customer Segmentation Using K-Means Clustering

## 📌 Project Overview

Customer segmentation is an important data analytics and machine learning technique used to divide a large customer base into smaller groups based on similar characteristics, preferences, and behavioral patterns.

Understanding customer behavior is essential for businesses because different customers have different purchasing habits, financial capabilities, and spending patterns. By grouping customers into meaningful segments, organizations can better understand their target audience and develop effective business and marketing strategies.

This project demonstrates the application of the **K-Means Clustering algorithm**, an unsupervised machine learning technique, to perform customer segmentation. The analysis focuses primarily on customer **Annual Income** and **Spending Score** to identify groups of customers with similar financial and purchasing behavior.

The project includes data loading, exploratory analysis, feature selection, feature scaling, determination of the optimal number of clusters using the Elbow Method, implementation of the K-Means algorithm, visualization of customer segments, and analysis of the resulting clusters.

---

# 🎯 Project Objectives

The primary objective of this project is to apply the K-Means Clustering algorithm to identify meaningful customer segments.

The specific objectives are:

* To understand the concept of customer segmentation.
* To perform exploratory analysis on customer data.
* To identify relevant features for clustering.
* To prepare the dataset for machine learning analysis.
* To perform feature scaling using StandardScaler.
* To determine the optimal number of clusters using the Elbow Method.
* To implement the K-Means Clustering algorithm.
* To assign customers to different clusters based on their characteristics.
* To visualize customer segments using graphical representations.
* To identify the centroid of each cluster.
* To analyze customer behavior within different segments.
* To generate a final dataset containing customer cluster labels.
* To demonstrate the practical application of unsupervised machine learning.

---

# 📚 Introduction

Businesses collect large amounts of customer data from different sources, including purchases, transactions, customer profiles, online activities, and feedback.

However, analyzing all customers as a single group may not provide meaningful insights because customers often have significantly different characteristics and spending habits.

Customer segmentation helps solve this problem by dividing customers into smaller groups based on similarities in their data.

For example, a business may identify:

* Customers with high income and high spending behavior.
* Customers with high income but low spending behavior.
* Customers with low income and high spending behavior.
* Customers with low income and low spending behavior.
* Customers with moderate income and moderate spending patterns.

These groups can help organizations understand customer behavior and develop personalized strategies.

In this project, the **K-Means Clustering algorithm** is used to automatically identify customer groups from the dataset.

---

# 📊 Dataset Description

The dataset used in this project is:

```text
customer_segmentation_kmeans_dataset.csv
```

The dataset contains customer information that can be used to analyze customer characteristics and spending behavior.

The dataset includes the following features:

| Feature                | Description                                              |
| ---------------------- | -------------------------------------------------------- |
| CustomerID             | Unique identification number assigned to each customer   |
| Gender                 | Gender of the customer                                   |
| Age                    | Age of the customer                                      |
| Annual Income (k$)     | Annual income of the customer in thousands of dollars    |
| Spending Score (1-100) | Score representing the spending behavior of the customer |

---

## 📌 Features Used for Clustering

Although the dataset contains multiple features, this project primarily uses the following features for customer segmentation:

### 1. Annual Income (k$)

Annual Income represents the financial capacity of a customer.

Customers with similar income levels may demonstrate similar purchasing capabilities.

### 2. Spending Score (1-100)

The Spending Score represents the spending behavior of a customer.

A higher spending score generally indicates higher customer spending behavior, while a lower score indicates lower spending behavior.

These two features provide a clear representation of customer financial and spending patterns and are suitable for visualization using a two-dimensional scatter plot.

---

# 🤖 Machine Learning Approach

## Unsupervised Machine Learning

This project uses an **Unsupervised Machine Learning** approach.

In supervised learning, the dataset contains predefined output labels, and the algorithm learns to predict those labels.

However, in unsupervised learning, the dataset does not contain predefined categories.

The algorithm automatically identifies patterns and relationships within the data.

In this project, customers are not initially assigned to predefined customer groups.

The K-Means algorithm automatically groups customers based on similarities between their income and spending behavior.

---

# 🔷 K-Means Clustering Algorithm

K-Means is one of the most widely used clustering algorithms in machine learning and data analysis.

The purpose of K-Means is to divide data points into a specified number of groups called **clusters**.

Each cluster contains data points that are more similar to one another than to data points in other clusters.

The value of **K** represents the number of clusters.

---

## ⚙️ How K-Means Works

The K-Means algorithm follows the steps below:

### Step 1: Select the Number of Clusters

The number of clusters, represented by **K**, is selected.

For example:

```text
K = 5
```

means that the dataset will be divided into five different customer groups.

---

### Step 2: Initialize Cluster Centroids

The algorithm selects initial points called **centroids**.

A centroid represents the center of a cluster.

---

### Step 3: Calculate Distance

The algorithm calculates the distance between each customer data point and the available cluster centroids.

---

### Step 4: Assign Customers to Clusters

Each customer is assigned to the cluster with the nearest centroid.

---

### Step 5: Recalculate Centroids

After assigning customers to clusters, new centroid positions are calculated.

---

### Step 6: Repeat the Process

The algorithm continues assigning customers and recalculating centroids until the clusters become stable.

The final output is a set of customer groups with similar characteristics.

---

# 📈 Data Preprocessing

Data preprocessing is an important stage in any machine learning project.

Before applying the K-Means algorithm, the dataset must be prepared for analysis.

The preprocessing steps in this project include:

* Loading the dataset.
* Exploring the dataset structure.
* Checking data types.
* Checking for missing values.
* Generating statistical summaries.
* Selecting relevant features.
* Scaling numerical features.

---

# 🔍 Exploratory Data Analysis

Exploratory Data Analysis (EDA) is performed to understand the structure and characteristics of the dataset.

The analysis includes:

* Viewing the first few records.
* Checking the number of rows and columns.
* Identifying dataset features.
* Examining data types.
* Checking for missing values.
* Generating descriptive statistics.

This step helps ensure that the dataset is suitable for clustering analysis.

---

# 🧹 Missing Value Analysis

Missing values can affect the performance and accuracy of machine learning algorithms.

The dataset is checked for missing values using Pandas.

```python
df.isnull().sum()
```

If missing values are present, appropriate preprocessing techniques should be applied before training the clustering model.

---

# 📊 Statistical Analysis

A statistical summary is generated to understand the numerical characteristics of the dataset.

```python
df.describe()
```

The statistical summary provides information such as:

* Count
* Mean
* Standard Deviation
* Minimum Value
* Maximum Value
* 25th Percentile
* 50th Percentile
* 75th Percentile

This information helps in understanding the distribution of customer characteristics.

---

# ⚖️ Feature Scaling

Feature scaling is performed before applying the K-Means algorithm.

The selected features may have different numerical ranges.

For example:

* Annual Income may have values ranging across larger numerical values.
* Spending Score has values between 1 and 100.

Without feature scaling, features with larger numerical values may have a greater influence on the clustering process.

To avoid this issue, **StandardScaler** is used.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_scaled = scaler.fit_transform(X)
```

Feature scaling ensures that both selected features contribute appropriately to the clustering process.

---

# 📉 Elbow Method

One of the important challenges in K-Means Clustering is selecting the appropriate number of clusters.

The **Elbow Method** is used to determine the optimal value of K.

The method calculates the **Within-Cluster Sum of Squares (WCSS)** for different numbers of clusters.

---

## What is WCSS?

WCSS represents the total squared distance between each data point and the centroid of its assigned cluster.

A lower WCSS value generally indicates that data points are closer to their cluster centroids.

However, increasing the number of clusters will naturally decrease WCSS.

The Elbow Method helps identify a suitable balance between:

* Too few clusters.
* Too many clusters.

The optimal number of clusters is selected at the point where the graph forms an elbow-like shape.

---

# 📊 Customer Segmentation Process

The customer segmentation process includes the following stages:

```text
Customer Dataset
       │
       ▼
Data Exploration
       │
       ▼
Data Preprocessing
       │
       ▼
Feature Selection
       │
       ▼
Feature Scaling
       │
       ▼
Elbow Method
       │
       ▼
Optimal Number of Clusters
       │
       ▼
K-Means Clustering
       │
       ▼
Customer Cluster Assignment
       │
       ▼
Visualization and Analysis
```

---

# 📈 Cluster Visualization

The customer segments generated by the K-Means algorithm are visualized using scatter plots.

The visualization includes:

* **X-axis:** Annual Income (k$)
* **Y-axis:** Spending Score (1-100)
* **Colors:** Different customer clusters

The scatter plot helps visually identify customer groups and understand the relationship between income and spending behavior.

---

# 🎯 Cluster Centroids

Each cluster contains a central point known as a **centroid**.

The centroid represents the average position of the customers belonging to that cluster.

Cluster centroids are displayed along with customer data points to provide a better understanding of the clustering structure.

The visualization includes:

* Customer data points.
* Different customer clusters.
* Cluster centroids.

---

# 📊 Customer Segment Analysis

After clustering, customers are divided into groups based on similarities in Annual Income and Spending Score.

The clusters may represent different customer behavior patterns, such as:

### High Income – High Spending

Customers in this segment have a high annual income and a high spending score.

These customers may represent valuable customers for businesses.

---

### High Income – Low Spending

Customers in this segment have a high annual income but a lower spending score.

Businesses may analyze this group to understand why their spending behavior is lower.

---

### Low Income – High Spending

Customers in this group have lower income but higher spending behavior.

This segment may demonstrate strong purchasing interest despite having a lower income level.

---

### Low Income – Low Spending

Customers in this group have lower income and lower spending behavior.

Businesses may develop appropriate strategies for this customer segment.

---

### Moderate Income – Moderate Spending

Customers in this group demonstrate average income and spending behavior.

This segment may represent the general customer population.

---

# 💼 Business Applications

Customer segmentation has several practical business applications.

## 🎯 Targeted Marketing

Businesses can create personalized marketing campaigns for different customer groups.

Instead of using the same strategy for all customers, companies can develop targeted campaigns.

---

## 💰 Customer Value Analysis

Customer segmentation can help businesses identify high-value customers.

These customers can receive special offers, rewards, and personalized services.

---

## 🛍️ Product Recommendations

Customer segments can be used to recommend suitable products based on customer characteristics and behavior.

---

## 🤝 Customer Retention

Businesses can identify valuable customer segments and develop strategies to improve customer satisfaction and retention.

---

## 📈 Data-Driven Decision Making

Customer segmentation provides meaningful insights that can support business decisions.

Organizations can use the results to improve:

* Marketing strategies.
* Customer service.
* Product development.
* Business planning.

---

# 🛠️ Technologies Used

The following technologies and tools are used in this project:

### Programming Language

* Python

### Development Environment

* Google Colab

### Libraries

* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

# 📚 Library Description

## Pandas

Pandas is used for:

* Loading CSV files.
* Data manipulation.
* Data analysis.
* Data preprocessing.

---

## NumPy

NumPy is used for numerical computations and array operations.

---

## Matplotlib

Matplotlib is used for:

* Creating graphs.
* Visualizing the Elbow Method.
* Displaying customer clusters.
* Displaying cluster centroids.

---

## Scikit-learn

Scikit-learn is used for machine learning tasks.

The following modules are used:

```python
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler
```

---

# ⚙️ Project Workflow

The complete workflow of the project is:

### Step 1: Import Required Libraries

Import the required Python libraries for data analysis, visualization, and machine learning.

---

### Step 2: Upload the Dataset

Upload the dataset file:

```text
customer_segmentation_kmeans_dataset.csv
```

---

### Step 3: Load the Dataset

Load the dataset using Pandas.

```python
df = pd.read_csv("customer_segmentation_kmeans_dataset.csv")
```

---

### Step 4: Explore the Dataset

Examine the dataset using:

* `df.head()`
* `df.shape`
* `df.info()`

---

### Step 5: Check Missing Values

Check for missing values using:

```python
df.isnull().sum()
```

---

### Step 6: Generate Statistical Summary

Generate descriptive statistics using:

```python
df.describe()
```

---

### Step 7: Select Features

Select the features used for clustering.

```python
X = df[
    [
        "Annual Income (k$)",
        "Spending Score (1-100)"
    ]
]
```

---

### Step 8: Perform Feature Scaling

Scale the selected features using StandardScaler.

---

### Step 9: Apply the Elbow Method

Calculate WCSS values for different values of K.

---

### Step 10: Visualize the Elbow Method

Create a graph to identify the optimal number of clusters.

---

### Step 11: Train the K-Means Model

Train the K-Means Clustering algorithm using the selected number of clusters.

---

### Step 12: Assign Cluster Labels

Assign the generated cluster labels to the original dataset.

---

### Step 13: Visualize Customer Segments

Create a scatter plot to visualize the different customer groups.

---

### Step 14: Display Cluster Centroids

Visualize the cluster centroids.

---

### Step 15: Analyze Customer Clusters

Calculate average characteristics for each cluster.

---

### Step 16: Save the Final Result

Save the segmented customer dataset.

---

# 📂 Project Structure

```text
customer-segmentation-kmeans/
│
├── Customer_Segmentation_Using_K_Means_Clustering.ipynb
│
├── customer_segmentation_kmeans_dataset.csv
│
├── Customer_Segmentation_Result.csv
│
└── README.md
```

---

# ▶️ How to Run the Project

## Step 1: Download or Clone the Repository

Download the project files from the GitHub repository.

---

## Step 2: Open the Notebook

Open the following notebook:

```text
Customer_Segmentation_Using_K_Means_Clustering.ipynb
```

The notebook can be opened using:

* Google Colab
* Jupyter Notebook

---

## Step 3: Upload the Dataset

Upload:

```text
customer_segmentation_kmeans_dataset.csv
```

---

## Step 4: Install Required Libraries

If required, install the necessary Python libraries.

```python
pip install pandas numpy matplotlib scikit-learn
```

---

## Step 5: Run All Cells

Run the notebook cells sequentially.

The program will:

* Load the dataset.
* Explore the dataset.
* Check for missing values.
* Perform feature selection.
* Apply feature scaling.
* Use the Elbow Method.
* Train the K-Means model.
* Generate customer clusters.
* Visualize the clustering results.
* Analyze the customer segments.

---

# 📌 Expected Output

The project generates the following outputs:

* Dataset preview.
* Dataset information.
* Missing value analysis.
* Statistical summary.
* Selected features.
* Feature scaling results.
* Elbow Method graph.
* WCSS values.
* Customer segmentation visualization.
* Cluster centroid visualization.
* Cluster analysis.
* Final segmented dataset.

---

# 📄 Final Output Dataset

After completing the clustering process, the final dataset is saved as:

```text
Customer_Segmentation_Result.csv
```

The output dataset contains the original customer information along with an additional cluster column.

Example structure:

| CustomerID | Gender | Age | Annual Income (k$) | Spending Score (1-100) | Cluster |
| ---------- | ------ | --- | ------------------ | ---------------------- | ------- |
| 1          | Male   | 19  | 15                 | 39                     | 0       |
| 2          | Male   | 21  | 15                 | 81                     | 1       |

---

# 🎓 Learning Outcomes

After completing this project, the following concepts are demonstrated:

* Python programming.
* Dataset handling using Pandas.
* Exploratory Data Analysis.
* Data preprocessing.
* Feature selection.
* Feature scaling.
* Unsupervised Machine Learning.
* K-Means Clustering.
* Elbow Method.
* WCSS analysis.
* Cluster centroid analysis.
* Data visualization.
* Customer behavior analysis.

---

# 🔮 Future Enhancements

This project can be extended in the future by implementing additional features and advanced machine learning techniques.

Possible future enhancements include:

* Using additional customer features for segmentation.
* Applying Hierarchical Clustering.
* Applying DBSCAN Clustering.
* Comparing multiple clustering algorithms.
* Performing advanced customer behavior analysis.
* Creating interactive dashboards using Streamlit.
* Integrating real-time customer data.
* Developing personalized recommendation systems.
* Deploying the project as a web application.
* Integrating business intelligence dashboards.

---

# ⚠️ Limitations

The K-Means algorithm has certain limitations:

* The number of clusters must be selected before training.
* The algorithm may be sensitive to outliers.
* Results depend on the selected features.
* Different datasets may require different preprocessing techniques.
* K-Means works best when clusters are relatively well-separated.

---

# 📋 Requirements

The project requires the following Python libraries:

```text
pandas
numpy
matplotlib
scikit-learn
```

---

# 👩‍💻 Author

**Premalatha Venkatesan**

B.Tech – Artificial Intelligence and Data Science

---

# 📄 Conclusion

This project demonstrates the practical application of **K-Means Clustering for Customer Segmentation**.

By analyzing customer Annual Income and Spending Score, the K-Means algorithm groups customers with similar financial and spending characteristics into meaningful clusters.

The project demonstrates important concepts in data science and machine learning, including:

* Data preprocessing.
* Exploratory Data Analysis.
* Feature scaling.
* Unsupervised Machine Learning.
* K-Means Clustering.
* Elbow Method.
* Cluster visualization.
* Customer behavior analysis.

The generated customer segments can provide valuable insights into different customer groups and can support businesses in developing targeted marketing strategies and improving customer engagement.

This project serves as a practical example of how unsupervised machine learning can be applied to real-world business data to discover hidden patterns and meaningful customer segments.


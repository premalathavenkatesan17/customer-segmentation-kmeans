# Customer Segmentation Using K-Means Clustering

## 📌 Project Overview

Customer segmentation is the process of dividing customers into different groups based on similar characteristics and behavior. It helps businesses understand their customers and develop more effective marketing and business strategies.

This project implements the **K-Means Clustering algorithm** to segment customers based on their characteristics. The primary focus of the analysis is on customer **Annual Income** and **Spending Score**.

The K-Means algorithm is an **unsupervised machine learning algorithm**, meaning that it identifies patterns and groups in the data without requiring predefined output labels.

---

## 🎯 Objectives

The objectives of this project are:

* To perform customer segmentation using K-Means Clustering.
* To explore and understand the customer dataset.
* To analyze customer age, annual income, and spending behavior.
* To check the dataset for missing values.
* To select appropriate features for clustering.
* To standardize the selected features using StandardScaler.
* To determine the optimal number of clusters using the Elbow Method.
* To train a K-Means Clustering model.
* To assign customers to different clusters.
* To visualize customer segments.
* To analyze the characteristics of each customer group.
* To save the final dataset with cluster labels.

---

## 📊 Dataset

The dataset used for this project contains customer information.

### Dataset Columns

| Column Name       | Description                                              |
| ----------------- | -------------------------------------------------------- |
| `CustomerID`      | Unique identification number assigned to each customer   |
| `Age`             | Age of the customer                                      |
| `Annual_Income_k` | Annual income of the customer                            |
| `Spending_Score`  | Score representing the spending behavior of the customer |

### Features Used for Clustering

The following features are used for the main clustering analysis:

* `Annual_Income_k`
* `Spending_Score`

These features help identify customers with similar financial capacity and spending behavior.

---

## 🤖 Machine Learning Algorithm

### K-Means Clustering

K-Means is an unsupervised machine learning algorithm used to group similar data points into clusters.

The algorithm works by:

1. Selecting the number of clusters (`K`).
2. Initializing cluster centroids.
3. Calculating the distance between data points and centroids.
4. Assigning each customer to the nearest cluster.
5. Recalculating the cluster centroids.
6. Repeating the process until the clusters become stable.

---

## ⚙️ Project Workflow

The project follows the workflow below:

```text
Customer Dataset
       │
       ▼
Data Loading
       │
       ▼
Data Exploration
       │
       ▼
Missing Value Analysis
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
Cluster Assignment
       │
       ▼
Data Visualization
       │
       ▼
Customer Segment Analysis
```

---

## 🔍 Exploratory Data Analysis

Before applying the K-Means algorithm, the dataset is explored to understand its structure and characteristics.

The following operations are performed:

* Displaying the first few rows of the dataset.
* Checking the dataset dimensions.
* Checking data types.
* Checking for missing values.
* Generating descriptive statistics.

Typical functions used include:

```python
df.head()
df.shape
df.info()
df.describe()
```

---

## 🧹 Data Preprocessing

Data preprocessing is performed before applying the clustering algorithm.

The preprocessing steps include:

* Checking for missing values.
* Selecting relevant numerical features.
* Preparing the data for clustering.
* Standardizing features using `StandardScaler`.

---

## ⚖️ Feature Scaling

Feature scaling is important because the selected features may have different numerical ranges.

For example:

* `Annual_Income_k` may have a larger range of values.
* `Spending_Score` may have values within a different range.

To ensure that both features contribute equally to the clustering process, `StandardScaler` is used.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

---

## 📉 Elbow Method

The **Elbow Method** is used to determine the optimal number of clusters.

The method calculates the **Within-Cluster Sum of Squares (WCSS)** for different values of `K`.

The optimal number of clusters is selected by observing the point where the WCSS graph forms an elbow-like shape.

### WCSS

WCSS measures the total squared distance between data points and the centroid of their assigned cluster.

A lower WCSS value generally indicates that data points are closer to their respective cluster centroids.

---

## 📊 Feature Selection

The following features are selected for clustering:

```python
X = df[[
    "Annual_Income_k",
    "Spending_Score"
]]
```

These features are used because they provide meaningful information about customer income and spending behavior.

---

## 📈 Customer Segmentation

After identifying the optimal number of clusters, the K-Means algorithm is trained using the scaled dataset.

Each customer is assigned a cluster label.

For example:

```text
Customer 1 → Cluster 0
Customer 2 → Cluster 1
Customer 3 → Cluster 2
```

Customers within the same cluster have similar characteristics based on their annual income and spending score.

---

## 📉 Data Visualization

The clustering results are visualized using a scatter plot.

The visualization represents:

* **X-axis:** Annual Income
* **Y-axis:** Spending Score
* **Different colors:** Different customer clusters

The visualization helps identify patterns and relationships between customer income and spending behavior.

---

## 🎯 Cluster Analysis

The generated clusters may represent different customer groups, such as:

### High Income – High Spending

Customers with high annual income and high spending behavior.

These customers may represent high-value customers.

### High Income – Low Spending

Customers with high income but lower spending behavior.

Businesses may develop strategies to improve engagement with this group.

### Low Income – High Spending

Customers with lower income but higher spending behavior.

These customers may show strong purchasing interest.

### Low Income – Low Spending

Customers with lower income and lower spending behavior.

### Moderate Income – Moderate Spending

Customers with average income and moderate spending behavior.

> **Note:** The exact characteristics of each cluster depend on the results generated by the K-Means model.

---

## 💼 Business Applications

Customer segmentation can support several business applications.

### 🎯 Targeted Marketing

Businesses can create personalized marketing campaigns for different customer groups.

### 💰 Customer Value Analysis

Businesses can identify high-value customer segments.

### 🛍️ Personalized Recommendations

Businesses can recommend products based on customer characteristics and behavior.

### 🤝 Customer Retention

Businesses can develop strategies to improve customer satisfaction and retention.

### 📈 Data-Driven Decision Making

Customer segmentation provides useful insights for improving marketing and business strategies.

---

## 🛠️ Technologies Used

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

## 📚 Libraries and Their Purpose

| Library      | Purpose                                |
| ------------ | -------------------------------------- |
| Pandas       | Data loading and data manipulation     |
| NumPy        | Numerical operations                   |
| Matplotlib   | Data visualization                     |
| Scikit-learn | K-Means Clustering and feature scaling |

---

## 🚀 Implementation Steps

### Step 1: Import Required Libraries

Import the required libraries for data analysis, visualization, and machine learning.

### Step 2: Load the Dataset

Load the customer segmentation dataset using Pandas.

### Step 3: Explore the Dataset

Analyze the dataset structure, data types, and statistical information.

### Step 4: Check Missing Values

Identify whether the dataset contains missing values.

### Step 5: Select Features

Select `Annual_Income_k` and `Spending_Score` for clustering.

### Step 6: Perform Feature Scaling

Standardize the selected features using `StandardScaler`.

### Step 7: Apply the Elbow Method

Calculate WCSS for multiple values of `K`.

### Step 8: Identify the Optimal Number of Clusters

Select an appropriate number of clusters based on the Elbow Method graph.

### Step 9: Train the K-Means Model

Apply the K-Means algorithm to the scaled dataset.

### Step 10: Assign Cluster Labels

Add the generated cluster labels to the original dataset.

### Step 11: Visualize Customer Segments

Create a scatter plot to visualize the customer clusters.

### Step 12: Save the Results

Save the final dataset containing the assigned cluster labels.

---

## 📂 Project Structure

```text
customer-segmentation-kmeans/
│
├── Customer_Segmentation_Using_K_Means_Clustering.ipynb
├── customer_segmentation_kmeans_dataset.csv
├── Customer_Segmentation_Result.csv
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone or Download the Repository

Download or clone this repository to your local system.

### 2. Open the Notebook

Open the Jupyter Notebook file using:

* Google Colab
* Jupyter Notebook

### 3. Upload the Dataset

Ensure that the customer segmentation dataset is available in the working directory.

### 4. Install Required Libraries

Install the required libraries if necessary:

```bash
pip install pandas numpy matplotlib scikit-learn
```

### 5. Run the Notebook

Run all cells sequentially.

The notebook will:

* Load the dataset.
* Explore the data.
* Check for missing values.
* Select relevant features.
* Scale the features.
* Apply the Elbow Method.
* Train the K-Means model.
* Assign customer clusters.
* Visualize the segmentation results.
* Save the final output dataset.

---

## 📌 Expected Output

The project generates the following outputs:

* Dataset preview.
* Dataset information.
* Missing value analysis.
* Statistical summary.
* Feature scaling.
* Elbow Method graph.
* Optimal cluster selection.
* Customer segmentation visualization.
* Cluster analysis.
* Final dataset with cluster labels.

---

## 📄 Output Dataset

After applying K-Means Clustering, the final dataset contains an additional column:

```text
Cluster
```

This column indicates the cluster assigned to each customer.

Example:

| CustomerID | Age | Annual_Income_k | Spending_Score | Cluster |
| ---------- | --: | --------------: | -------------: | ------: |
| 1          |  19 |              15 |             39 |       0 |
| 2          |  21 |              16 |             81 |       1 |

---

## 🎓 Learning Outcomes

This project demonstrates the following concepts:

* Python programming.
* Data loading using Pandas.
* Exploratory Data Analysis.
* Data preprocessing.
* Feature selection.
* Feature scaling.
* Unsupervised machine learning.
* K-Means Clustering.
* Elbow Method.
* WCSS analysis.
* Cluster analysis.
* Data visualization.
* Customer behavior analysis.

---

## 🔮 Future Enhancements

This project can be extended by:

* Using additional customer features.
* Performing clustering using Age, Income, and Spending Score.
* Comparing K-Means with Hierarchical Clustering.
* Applying DBSCAN Clustering.
* Using the Silhouette Score to evaluate clusters.
* Creating an interactive dashboard using Streamlit.
* Building a customer analytics web application.
* Integrating real-time customer data.
* Developing personalized recommendation systems.

---

## ⚠️ Limitations

The K-Means algorithm has some limitations:

* The number of clusters must be specified before training.
* The algorithm may be sensitive to outliers.
* Results depend on the selected features.
* Different feature scaling methods may affect the results.
* K-Means works best when clusters are reasonably well-separated.

---

## 📋 Requirements

The following Python libraries are required:

```text
pandas
numpy
matplotlib
scikit-learn
```

---

## 👩‍💻 Author

**Premalatha Venkatesan**

B.Tech – Artificial Intelligence and Data Science

---

## 📄 Conclusion

This project demonstrates the practical application of the **K-Means Clustering algorithm for customer segmentation**.

Using customer information such as **Annual Income** and **Spending Score**, the algorithm identifies groups of customers with similar financial and spending characteristics.

The project demonstrates important concepts in data science and machine learning, including data preprocessing, feature scaling, unsupervised learning, the Elbow Method, K-Means Clustering, and data visualization.

The generated customer segments can help businesses better understand customer behavior and support targeted marketing strategies and data-driven decision-making.

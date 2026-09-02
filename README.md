# Customer Segmentation Using K-Means Clustering

## 📌 Project Overview

Customer segmentation is a data analysis technique used to divide customers into different groups based on similar characteristics, preferences, and purchasing behavior.

In this project, the **K-Means Clustering algorithm** is used to perform customer segmentation. Customers are grouped based on their **Annual Income** and **Spending Score**.

The purpose of this project is to identify meaningful customer groups and gain insights into customer behavior. These insights can help businesses develop better marketing strategies and improve customer relationships.

---

## 🎯 Project Objectives

The main objectives of this project are:

* To understand the concept of customer segmentation.
* To perform data preprocessing and exploratory data analysis.
* To select relevant features for clustering.
* To apply feature scaling using StandardScaler.
* To determine the optimal number of clusters using the Elbow Method.
* To implement the K-Means Clustering algorithm.
* To group customers based on similar income and spending behavior.
* To visualize the generated customer clusters.
* To analyze the characteristics of each customer segment.
* To generate a final dataset containing cluster labels.

---

## 📊 Dataset Description

The dataset contains information about customers and their spending behavior.

The features available in the dataset include:

| Feature                | Description                                            |
| ---------------------- | ------------------------------------------------------ |
| CustomerID             | Unique identification number assigned to each customer |
| Gender                 | Gender of the customer                                 |
| Age                    | Age of the customer                                    |
| Annual Income (k$)     | Annual income of the customer in thousands of dollars  |
| Spending Score (1-100) | Score assigned based on customer spending behavior     |

### Features Used for Clustering

The following two features are selected for customer segmentation:

* **Annual Income (k$)**
* **Spending Score (1-100)**

These features help identify customers with similar financial capacity and spending patterns.

---

## 🛠️ Technologies and Libraries Used

### Programming Language

* Python

### Development Environment

* Google Colab

### Python Libraries

* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## 📚 Machine Learning Concept

### Unsupervised Learning

This project uses **Unsupervised Machine Learning**.

Unlike supervised learning, unsupervised learning does not require predefined output labels. The algorithm automatically identifies patterns and groups similar data points.

---

## 🤖 K-Means Clustering Algorithm

K-Means is one of the most popular unsupervised machine learning algorithms.

The algorithm divides the dataset into a predefined number of groups called **clusters**.

### Working of K-Means

The K-Means algorithm follows these steps:

1. Select the number of clusters (K).
2. Initialize cluster centroids.
3. Assign each data point to the nearest centroid.
4. Calculate new centroids based on the assigned data points.
5. Repeat the process until the centroids no longer change significantly.

The final output consists of different groups of customers with similar characteristics.

---

## ⚙️ Project Workflow

The project follows the following workflow:

### Step 1: Import Required Libraries

Required Python libraries are imported for:

* Data manipulation
* Data analysis
* Visualization
* Machine learning

---

### Step 2: Upload the Dataset

The customer dataset is uploaded into the Google Colab environment.

---

### Step 3: Load the Dataset

The dataset is loaded using the Pandas library.

```python
df = pd.read_csv("Mall_Customers.csv")
```

---

### Step 4: Explore the Dataset

The dataset is explored to understand:

* Number of rows and columns
* Feature names
* Data types
* Dataset structure

---

### Step 5: Check for Missing Values

The dataset is checked for missing values to ensure data quality.

```python
df.isnull().sum()
```

---

### Step 6: Statistical Analysis

Statistical information about numerical features is generated using:

```python
df.describe()
```

This provides information such as:

* Mean
* Minimum value
* Maximum value
* Standard deviation
* Quartiles

---

### Step 7: Feature Selection

The relevant features selected for clustering are:

* Annual Income
* Spending Score

These features are used as input for the K-Means algorithm.

---

### Step 8: Feature Scaling

Feature scaling is performed using **StandardScaler**.

Feature scaling ensures that all selected features contribute equally to the clustering process.

---

### Step 9: Elbow Method

The Elbow Method is used to determine the optimal number of clusters.

The algorithm calculates the **Within-Cluster Sum of Squares (WCSS)** for different values of K.

The optimal value of K is selected by identifying the point where the graph forms an elbow.

---

## 📈 Within-Cluster Sum of Squares (WCSS)

WCSS represents the total distance between data points and their corresponding cluster centroid.

A lower WCSS value indicates that data points are closer to their cluster centroid.

The Elbow Method helps determine the balance between:

* Too few clusters
* Too many clusters

---

## 📊 Customer Segmentation

After determining the optimal number of clusters, the K-Means algorithm is trained on the scaled customer data.

Each customer is assigned a cluster label.

Example:

```text
Customer 1 → Cluster 0
Customer 2 → Cluster 1
Customer 3 → Cluster 2
```

Customers belonging to the same cluster have similar characteristics.

---

## 📉 Data Visualization

The clustering results are visualized using scatter plots.

The visualization displays:

* Annual Income on the X-axis
* Spending Score on the Y-axis
* Different colors representing different clusters

This visualization makes it easier to understand the relationship between income and spending behavior.

---

## 🎯 Cluster Centroids

Each cluster has a central point called a **centroid**.

The centroid represents the average position of all customers within a cluster.

The project visualizes:

* Customer data points
* Customer clusters
* Cluster centroids

---

## 📊 Results and Analysis

The K-Means algorithm successfully divides customers into different groups based on their income and spending patterns.

The customer groups can represent different types of customers, such as:

* Customers with high income and high spending.
* Customers with high income and low spending.
* Customers with low income and high spending.
* Customers with low income and low spending.
* Customers with moderate income and moderate spending.

These groups can help businesses understand different customer categories.

---

## 💼 Business Applications

Customer segmentation can be useful in several business applications.

### Targeted Marketing

Businesses can create personalized marketing campaigns for different customer groups.

### Customer Retention

Businesses can identify valuable customers and develop strategies to retain them.

### Product Recommendations

Customer segments can help businesses recommend suitable products.

### Business Decision Making

Customer data can support data-driven decision-making.

### Personalized Services

Businesses can provide customized services based on customer behavior.

---

## 📂 Project Structure

```text
customer-segmentation-kmeans/
│
├── Customer_Segmentation_Using_K_Means_Clustering.ipynb
│
├── Mall_Customers.csv
│
├── Customer_Segmentation_Result.csv
│
└── README.md
```

---

## ▶️ How to Run the Project

### Step 1

Clone or download the repository.

### Step 2

Open the notebook using one of the following platforms:

* Google Colab
* Jupyter Notebook

### Step 3

Upload the customer dataset.

### Step 4

Install the required libraries if necessary.

```python
pip install pandas numpy matplotlib scikit-learn
```

### Step 5

Run all notebook cells sequentially.

### Step 6

The program will:

* Load the dataset.
* Process the data.
* Perform feature scaling.
* Apply the Elbow Method.
* Train the K-Means model.
* Generate customer clusters.
* Display visualizations.

### Step 7

The final segmented dataset will be saved successfully.

---

## 📌 Expected Output

The project generates the following outputs:

* Dataset preview
* Dataset information
* Missing value analysis
* Statistical summary
* Elbow Method graph
* Optimal number of clusters
* Customer cluster visualization
* Cluster centroid visualization
* Customer segment analysis
* Final segmented customer dataset

---

## 🎓 Learning Outcomes

Through this project, the following concepts are learned and demonstrated:

* Python programming
* Data analysis using Pandas
* Data preprocessing
* Exploratory Data Analysis
* Feature selection
* Feature scaling
* Unsupervised Machine Learning
* K-Means Clustering
* Elbow Method
* Cluster analysis
* Data visualization
* Business data analysis

---

## 🔮 Future Enhancements

The project can be further improved by adding:

* Additional customer features for clustering.
* Advanced visualization techniques.
* Hierarchical Clustering.
* DBSCAN Clustering.
* Customer recommendation systems.
* Interactive dashboards using Streamlit.
* Real-time customer data analysis.
* Automated cluster labeling.
* Deployment as a web application.

---

## ⚠️ Limitations

The project has the following limitations:

* The number of clusters must be selected before applying K-Means.
* K-Means is sensitive to outliers.
* Results may vary depending on feature selection.
* The algorithm works best when clusters have relatively similar shapes.

---

## 📋 Requirements

The following libraries are required:

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

This project demonstrates the application of the **K-Means Clustering algorithm for customer segmentation**.

By analyzing customer annual income and spending behavior, the algorithm successfully groups customers with similar characteristics into meaningful clusters.

The results provide valuable insights into customer behavior and can help businesses develop targeted marketing strategies, improve customer engagement, and support better decision-making.

This project also demonstrates the practical application of **Unsupervised Machine Learning**, **data preprocessing**, **feature scaling**, and **data visualization**.









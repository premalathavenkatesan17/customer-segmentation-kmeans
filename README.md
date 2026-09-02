# Customer Segmentation Using K-Means Clustering

## 📌 Overview

Customer segmentation is an important technique used to group customers based on similar characteristics and purchasing behavior.

This project uses the **K-Means Clustering algorithm** to segment customers based on their **Annual Income** and **Spending Score**. The generated customer groups can help businesses understand customer behavior and develop effective marketing strategies.

---

## 🎯 Objective

The main objectives of this project are:

* To perform customer segmentation using K-Means Clustering.
* To analyze customer behavior based on income and spending patterns.
* To determine the optimal number of clusters using the Elbow Method.
* To visualize customer segments.
* To analyze the characteristics of different customer groups.

---

## 📊 Dataset

The dataset contains customer information with the following features:

| Feature                | Description                                    |
| ---------------------- | ---------------------------------------------- |
| CustomerID             | Unique identification number for each customer |
| Gender                 | Gender of the customer                         |
| Age                    | Age of the customer                            |
| Annual Income (k$)     | Annual income of the customer                  |
| Spending Score (1-100) | Customer spending behavior score               |

---

## 🛠️ Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## 🤖 Machine Learning Algorithm

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** used to group similar data points into clusters.

In this project, customers are segmented based on:

* Annual Income
* Spending Score

Customers with similar characteristics are grouped into the same cluster.

---

## ⚙️ Project Workflow

1. Import the required libraries.
2. Upload and load the customer dataset.
3. Explore the dataset.
4. Check for missing values.
5. Select relevant features for clustering.
6. Perform feature scaling.
7. Apply the Elbow Method to determine the optimal number of clusters.
8. Train the K-Means Clustering model.
9. Assign cluster labels to customers.
10. Visualize customer segments.
11. Analyze cluster characteristics.
12. Save the final segmented dataset.

---

## 📈 Elbow Method

The Elbow Method is used to determine the optimal number of clusters.

It calculates the **Within-Cluster Sum of Squares (WCSS)** for different values of K. The optimal number of clusters is selected based on the point where the graph forms an elbow.

---

## 📊 Results

The K-Means algorithm segments customers into different groups based on their income and spending behavior.

These customer segments can help businesses:

* Identify high-value customers.
* Understand customer spending patterns.
* Develop targeted marketing strategies.
* Improve customer engagement.

---

## 📂 Project Structure

```text
customer-segmentation-kmeans/
│
├── Customer_Segmentation_Using_K_Means_Clustering.ipynb
├── Mall_Customers.csv
├── Customer_Segmentation_Result.csv
└── README.md
```

---

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Open the `.ipynb` notebook using **Google Colab** or **Jupyter Notebook**.
3. Upload the customer dataset.
4. Run all cells sequentially.
5. The K-Means model will generate customer clusters.
6. Visualizations will display the customer segments.
7. The final segmented dataset will be saved successfully.

---

## 📌 Output

The project generates:

* Dataset exploration results.
* Missing value analysis.
* Elbow Method graph.
* Customer segmentation visualization.
* Cluster analysis.
* Customer segment visualization with centroids.
* Final segmented customer dataset.

---

## 🎓 Learning Outcomes

Through this project, the following concepts are demonstrated:

* Data preprocessing
* Exploratory Data Analysis
* Feature scaling
* Unsupervised Machine Learning
* K-Means Clustering
* Elbow Method
* Data visualization
* Customer behavior analysis

---

## 👩‍💻 Author

**Premalatha Venkatesan**

B.Tech – Artificial Intelligence and Data Science

---

## 📄 Conclusion

This project demonstrates the use of the **K-Means Clustering algorithm** for customer segmentation. By grouping customers based on their annual income and spending behavior, the project provides meaningful insights into customer patterns and supports data-driven business decision-making.



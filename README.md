# 🛍️ Customer Segmentation using RFM and K-Means
This project segments customers of an online retail store based on their purchasing behavior using RFM analysis and K-Means clustering.
## 📊 Objective
To identify distinct customer segments to enable better targeting, personalized marketing, and customer retention strategies.
## 📁 Dataset
- **Name**: Online Retail Dataset  
- **Source**: UCI Machine Learning Repository  
- [Dataset Link](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
## 🔧 Process Overview
1. **Data Cleaning**
   - Removed missing Customer IDs  
   - Filtered out negative and zero values for `Quantity` and `UnitPrice`  
   - Converted `InvoiceDate` to datetime  
2. **RFM Analysis**
   - **Recency** = Days since last purchase  
   - **Frequency** = Number of unique invoices  
   - **Monetary** = Total spending per customer  
3. **Data Normalization**
   - Applied `StandardScaler` to RFM values for fair clustering  
4. **K-Means Clustering**
   - Used the Elbow Method to find the optimal number of clusters  
   - Segmented customers into 4 groups  
5. **Visualization**
   - Scatter plots for Recency vs Frequency, Monetary vs Frequency  
   - Bar chart of cluster sizes  
   - Cluster profile table  
## 📊 Sample Results
| Cluster | Recency (days) | Frequency | Monetary (total) | Segment Description            |
|---------|----------------|-----------|------------------|--------------------------------|
| 0       | Low  (e.g. 10) | High      | High             | Loyal, big spenders            |
| 1       | High (e.g. 180)| Low       | Low              | Inactive customers             |
| 2       | Mid  (e.g. 45) | Mid       | Mid              | Moderate, steady buyers        |
| 3       | Low  (e.g. 15) | Low       | Low              | New but infrequent customers   |

## 📈 Tech Stack
- Python  
- Pandas / NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  
- Google Colab  
## 🚀 How to Run
1. **Clone the repo**  
   ```bash
   git clone https://github.com/Yugandhar2807/customer-segmentation.git
   cd customer-segmentation

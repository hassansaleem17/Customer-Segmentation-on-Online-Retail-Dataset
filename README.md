# 🛍️ Customer Segmentation on Online Retail Dataset

This project segments customers using K-Means clustering based on Recency, Frequency, and Monetary (RFM) values to uncover actionable business insights.

---

## 📂 Files
- `model.ipynb` – Full Jupyter Notebook with data cleaning, feature engineering, and K-Means modeling.
- `Slides.pptx` – Presentation summarizing dataset analysis, cluster descriptions, and business actions.
- `README.md` – Project documentation for GitHub.

---

## 📊 Dataset Overview
- **Name**: Online Retail II
- **Records**: 538,000+
- **Columns**: 8 (4 categorical, 4 numerical)
- **Goal**: Segment customers into actionable groups

---

## 🧹 Data Cleaning
- Removed negative/zero price & quantity
- Excluded null `CustomerID` rows
- Filtered invalid invoices and stock codes
- Dropped ~23% of noisy or incomplete data

---

## ⚙️ Feature Engineering
- `SalesTotal` = `Price × Quantity`
- `MonetaryValue`: Total sales per customer
- `Frequency`: Unique invoices per customer
- `Recency`: Days since last purchase

---

## 🤖 Model Used
- **Algorithm**: K-Means Clustering
- **K Selection**: Elbow Method & Silhouette Score
- **Output**: 4 Customer Clusters

---

## 📈 Cluster Insights

| Cluster | Label       | Summary                                                                 | Business Action                              |
|--------:|-------------|-------------------------------------------------------------------------|-----------------------------------------------|
| 0       | Retain      | High value, frequent but not recent buyers                              | Loyalty programs, targeted re-engagement     |
| 1       | Re-Engage   | Low value, infrequent, and not recent                                   | Discounts, email marketing                   |
| 2       | Nurture     | New or low-spending but recent buyers                                   | Nurturing campaigns, onboarding offers       |
| 3       | Reward      | Very frequent and high-spending recent buyers                           | Exclusive deals, premium loyalty rewards     |

---

## 🚀 Run Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/customer-segmentation-retail.git
   cd customer-segmentation-retail

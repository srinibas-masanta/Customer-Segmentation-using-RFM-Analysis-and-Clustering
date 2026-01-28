# Customer Segmentation using RFM Analysis and K-Means Clustering

## 📌 Project Overview

Understanding customer behavior is critical for businesses aiming to improve retention, engagement, and revenue. However, transactional data is often noisy, unstructured, and lacks explicit labels that describe customer value or behavior.

This project applies **RFM (Recency, Frequency, Monetary) analysis** combined with **K-Means clustering** to segment customers based on their purchasing behavior. Using a real-world retail dataset, the goal is to uncover meaningful customer segments and translate them into **actionable business insights**.

The project demonstrates an end-to-end **unsupervised machine learning workflow**, covering data preprocessing, feature engineering, outlier handling, clustering, visualization, and interpretation.

---

## 🎯 Problem Statement

Online retailers often struggle to:

* Identify high-value and at-risk customers
* Understand behavioral differences across their customer base
* Design targeted marketing strategies instead of generic campaigns

The challenge is to segment customers **without labeled outcomes**, using only transactional data, while handling real-world issues such as missing values, skewed distributions, and extreme outliers.

---

## 🧠 Objective

* Segment customers based on purchasing behavior using **RFM features**
* Apply **K-Means clustering** to discover natural groupings
* Handle outliers separately to avoid distortion of clusters
* Translate clusters into **meaningful, business-oriented customer segments**
* Provide actionable recommendations for each segment

---

## 📂 Dataset

* **Dataset:** Online Retail II
* **Source:** UCI Machine Learning Repository
* **Description:** Transaction-level data from a UK-based online retailer containing invoice details, product information, prices, and customer IDs.

---

## 🛠️ Tools & Technologies

* **Programming Language:** Python
* **Libraries:**

  * `pandas`, `numpy` – data manipulation
  * `matplotlib`, `seaborn` – visualization
  * `scikit-learn` – scaling, clustering, evaluation

---

## 🔍 Project Workflow

### 1. Data Understanding & Exploration

* Examined dataset structure, data types, and missing values
* Identified inconsistencies such as missing customer IDs, invalid quantities, and pricing anomalies
* Explored distributions of key variables to understand data skewness and potential outliers

---

### 2. Data Cleaning & Preprocessing

* Removed records with missing or invalid customer information
* Filtered out unreliable transactions (e.g., negative or zero values)
* Retained only clean and meaningful transactions for analysis
* Approximately **23% of records were removed** to ensure data quality

---

### 3. Feature Engineering (RFM Analysis)

* Aggregated transaction-level data to the **customer level**
* Computed:

  * **Monetary Value:** Total spending per customer
  * **Frequency:** Number of unique invoices per customer
  * **Recency:** Days since the customer’s last purchase
* Created a structured RFM dataset representing customer behavior

---

### 4. Outlier Detection & Handling

* Identified extreme values in **Monetary** and **Frequency** using statistical thresholds
* Segmented outliers into:

  * Monetary-only outliers
  * Frequency-only outliers
  * Combined Monetary & Frequency outliers
* Temporarily removed outliers before clustering to avoid centroid distortion
* Analyzed outliers separately due to their high business importance

---

### 5. Feature Scaling

* Standardized RFM features using **StandardScaler**
* Ensured equal contribution of all features in distance-based clustering

---

### 6. K-Means Clustering

* Applied K-Means clustering on non-outlier customers
* Evaluated optimal number of clusters using:

  * **Elbow method (Inertia)**
  * **Silhouette score**
* Selected **4 clusters**, balancing cluster quality and business interpretability

---

### 7. Cluster Visualization & Interpretation

* Used **3D scatter plots** to visualize customer segmentation
* Applied **violin plots** to analyze feature distributions across clusters
* Compared clustered distributions against the overall population for context

---

### 8. Cluster Labeling (Business Segmentation)

Each cluster was assigned a meaningful, actionable label:

| Cluster Name  | Description                                           |
| ------------- | ----------------------------------------------------- |
| **RETAIN**    | Moderately active, balanced RFM customers             |
| **RE-ENGAGE** | Inactive customers with high recency                  |
| **NURTURE**   | Low-value but recently active customers               |
| **REWARD**    | High-frequency and high-spending loyal customers      |
| **PAMPER**    | High spenders with infrequent purchases               |
| **UPSELL**    | Frequent buyers with lower spend per purchase         |
| **DELIGHT**   | Extremely valuable customers (high spend & frequency) |

---

### 9. Combined Analysis & Insights

* Merged non-outlier clusters with outlier segments for a holistic view
* Used a **combined bar and line chart** to analyze:

  * Customer distribution across clusters
  * Average RFM values per segment
* Observed a classic pattern where:

  * A small number of customers drive a large portion of revenue
  * Most customers fall into low-to-mid engagement segments

---

## 📊 Key Business Insights

* **NURTURE** is the largest segment, indicating a broad base of low-engagement customers
* **RE-ENGAGE** customers represent strong reactivation opportunities
* **REWARD and DELIGHT** customers, though fewer in number, contribute disproportionately to revenue
* High-value outliers require **separate, premium strategies**
* Effective customer management requires **segment-specific strategies**, not a one-size-fits-all approach

---

## 🚀 Business Recommendations

* **NURTURE:** Gradual engagement, onboarding offers
* **RE-ENGAGE:** Targeted reactivation campaigns
* **RETAIN:** Consistent communication and loyalty maintenance
* **REWARD / DELIGHT / PAMPER / UPSELL:** Personalized offers, VIP programs, and premium experiences

---

## 🔮 Future Scope

* Incorporate **time-based analysis** to track customer movement between segments
* Apply **advanced clustering techniques** (e.g., DBSCAN, Gaussian Mixture Models)
* Integrate **predictive models** for churn or lifetime value estimation
* Deploy as a **dashboard or web application** for real-time insights

---

## 📚 References

* UCI Machine Learning Repository – Online Retail II Dataset
* Scikit-learn Documentation
* RFM Analysis Framework

---

## 🎓 Internship Context

This project was completed as part of a **6-week AI & Machine Learning internship** offered by **Edunet Foundation**, in collaboration with **AICTE**, under the **IBM SkillsBuild Program**.

* **Internship Duration:** December 10, 2025 – January 21, 2026
* **Focus Area:** Artificial Intelligence & Machine Learning
* **Mode:** Project-based, mentor-guided learning

The internship emphasized applying data science and machine learning techniques to real-world problems. This customer segmentation project was independently developed as the core deliverable, demonstrating end-to-end skills in data preprocessing, unsupervised learning, visualization, and business interpretation.

---

## ⭐ Final Note

This project demonstrates a complete, real-world application of **unsupervised learning for customer segmentation**, with a strong emphasis on **interpretability, business relevance, and actionable insights**. It is designed to be both a learning resource and a portfolio-ready project.

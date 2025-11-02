# 🛍️ Customer Shopping Behavior Analysis

## 📘 Project Overview
This project analyzes **customer shopping behavior** using transactional data from **3,900 purchases** across multiple product categories.  
The primary goal is to uncover insights into **spending patterns**, **customer segmentation**, **product preferences**, and **subscription behavior** to support strategic business decisions.

---

## 🧾 Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18  
- **Key Features:**
  - Customer demographics — *Age, Gender, Location, Subscription Status*  
  - Purchase details — *Item Purchased, Category, Purchase Amount, Season, Size, Color*  
  - Shopping behavior — *Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type*  
- **Missing Data:** 37 missing values in the `Review Rating` column  

---

## 🐍 Exploratory Data Analysis (Python)

### 🔹 Steps Performed
1. **Data Loading:** Imported the dataset using `pandas`.  
2. **Initial Exploration:**  
   - Used `df.info()` to understand data structure  
   - Used `df.describe()` for statistical summary  
3. **Missing Data Handling:**  
   - Imputed missing values in `Review Rating` column using **median rating per product category**.  
4. **Column Standardization:**  
   - Renamed columns to `snake_case` for readability.  
5. **Feature Engineering:**  
   - Created `age_group` by binning customer ages.  
   - Created `purchase_frequency_days` from timestamp data.  
6. **Data Consistency Check:**  
   - Verified redundancy between `discount_applied` and `promo_code_used`; dropped the latter.  
7. **Database Integration:**  
   - Connected Python script to **MySQL** and uploaded the cleaned dataset.

---

## 🧮 SQL Business Analysis (MySQL)

Structured queries were used to answer business-critical questions:

| # | Analysis | Objective |
|---|-----------|------------|
| 1 | **Revenue by Gender** | Compare total revenue from male vs. female customers |
| 2 | **High-Spending Discount Users** | Identify customers who use discounts but spend above average |
| 3 | **Top 5 Products by Rating** | Find highest-rated products |
| 4 | **Shipping Type Comparison** | Compare spending between Standard vs. Express shipping |
| 5 | **Subscribers vs. Non-Subscribers** | Compare average and total revenue |
| 6 | **Discount-Dependent Products** | Identify products most often bought on discount |
| 7 | **Customer Segmentation** | Classify customers into *New*, *Returning*, *Loyal* |
| 8 | **Top 3 Products per Category** | Find top-purchased items per category |
| 9 | **Repeat Buyers & Subscriptions** | Analyze correlation between repeat purchases and subscriptions |
| 10 | **Revenue by Age Group** | Calculate revenue contributions by age group |

---

## 📊 Power BI Dashboard

An interactive **Power BI dashboard** was built to visualize insights:
- Revenue trends by demographic segments  
- Purchase behavior by category  
- Discount vs. non-discount performance  
- Subscription and loyalty analytics  
- Product performance and customer retention metrics

![Dashboard Preview](https://github.com/Danieltech1026/customer-trends-data-analysis-SQL-Python-PowerBI/blob/main/customer%20behavior%20dashboard.png?raw=true)

---

## 💡 Business Recommendations

1. **Boost Subscriptions:** Offer exclusive benefits to subscribers.  
2. **Customer Loyalty Programs:** Reward repeat buyers to strengthen retention.  
3. **Review Discount Policy:** Balance sales boosts with profit margins.  
4. **Product Positioning:** Highlight top-rated and best-selling products.  
5. **Targeted Marketing:** Focus campaigns on high-value age groups and express-shipping users.  

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|----------|
| **Python (pandas, numpy, matplotlib, seaborn)** | Data cleaning, preprocessing, and EDA |
| **MySQL** | Structured business analysis via SQL |
| **Power BI** | Interactive data visualization |
| **Jupyter Notebook** | Analysis and documentation environment |

---

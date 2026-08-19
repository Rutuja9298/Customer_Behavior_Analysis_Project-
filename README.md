# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analytics project exploring customer shopping behavior using transactional data. The project covers data cleaning and feature engineering in **Python**, business analysis using **SQL (PostgreSQL)**, and interactive visualization in **Power BI** to uncover insights into spending patterns, customer segments, and subscription behavior.

---

## 📌 Project Overview

This project analyzes shopping behavior using transactional data from **3,900 purchases** across multiple product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

---

## 📊 Dataset Summary

- **Rows:** 3,900
- **Columns:** 18
- **Missing Data:** 37 missing values in the `Review Rating` column

**Key Features:**
- **Customer Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python (pandas)** | Data cleaning, preprocessing, feature engineering |
| **PostgreSQL** | Structured querying and business analysis |
| **SQLAlchemy** | Python–PostgreSQL database connection |
| **pgAdmin4** | Database management and query execution |
| **Power BI** | Interactive dashboard and data visualization |

---

## 🔍 Exploratory Data Analysis (Python)

- **Data Loading:** Imported the dataset using pandas
- **Initial Exploration:** Used `df.info()` and `.describe()` for structure and summary statistics
- **Missing Data Handling:** Imputed missing `Review Rating` values using the median rating of each product category
- **Column Standardization:** Renamed columns to snake_case for readability and consistency
- **Feature Engineering:**
  - Created `age_group` by binning customer ages
  - Created `purchase_frequency_days` from purchase data
- **Data Consistency Check:** Verified redundancy between `discount_applied` and `promo_code_used`; dropped `promo_code_used`
- **Database Integration:** Loaded the cleaned DataFrame into PostgreSQL using SQLAlchemy for SQL-based analysis

---

## 🧮 Business Analysis (SQL)

Structured SQL queries were used in PostgreSQL to answer key business questions:

1. **Revenue by Gender** — Male customers generated significantly higher revenue ($157,890) than female customers ($75,191)

<p align="center">
  <img src="images/revenue_by_gender.png" alt="Revenue by Gender" width="500"/>
</p>

2. **High-Spending Discount Users** — Identified 839 customers who used discounts but still spent above the average purchase amount
3. **Top 5 Products by Rating** — Gloves, Sandals, Boots, Hat, and Skirt had the highest average review ratings
4. **Shipping Type Comparison** — Express shipping customers spent slightly more on average ($60.48) than Standard shipping customers ($58.46)
5. **Subscribers vs. Non-Subscribers** — Non-subscribers contributed far higher total revenue ($170,436) despite a similar average spend
6. **Discount-Dependent Products** — Hat, Sneakers, Coat, Sweater, and Pants had the highest discount usage rates
7. **Customer Segmentation** — Classified customers into New (83), Returning (701), and Loyal (3,116) segments

<p align="center">
  <img src="images/customer_segmentation.png" alt="Customer Segmentation" width="500"/>
</p>

8. **Top 3 Products per Category** — Identified best-selling items within Accessories, Clothing, Footwear, and Outerwear
9. **Repeat Buyers & Subscriptions** — Analyzed whether customers with more than 5 purchases were more likely to subscribe
10. **Revenue by Age Group** — Young Adults generated the highest revenue ($62,143), followed by Middle-aged, Adult, and Senior groups

<p align="center">
  <img src="images/revenue_by_age_group.png" alt="Revenue by Age Group" width="500"/>
</p>

---

## 📈 Power BI Dashboard

An interactive **Customer Behavior Dashboard** was built in Power BI, featuring:

<p align="center">
  <img src="images/powerbi_dashboard.png" alt="Power BI Customer Behavior Dashboard" width="800"/>
</p>

- Key metrics: Number of Customers, Average Purchase Amount, Average Review Rating
- Customer distribution by Subscription Status
- Revenue and Sales breakdown by Category
- Revenue and Sales breakdown by Age Group
- Slicers for Subscription Status, Gender, Category, and Shipping Type

---

## 💡 Business Recommendations

- **Boost Subscriptions** — Promote exclusive benefits to convert non-subscribers, who currently drive the majority of revenue
- **Customer Loyalty Programs** — Reward repeat buyers to move them further into the "Loyal" segment
- **Review Discount Policy** — Balance promotional discounts with overall margin control
- **Product Positioning** — Highlight top-rated and best-selling products in marketing campaigns
- **Targeted Marketing** — Focus efforts on high-revenue age groups and express-shipping customers

---

## 📁 Project Structure

```
customer-shopping-behavior-analysis/
│
├── data/                   # Raw and cleaned datasets
├── notebooks/               # Python (pandas) EDA and cleaning scripts
├── sql/                      # SQL queries used for business analysis
├── dashboard/                # Power BI (.pbix) dashboard file
├── README.md                 # Project documentation
```

---

## 🚀 How to Reproduce

1. Clone the repository
2. Set up a PostgreSQL database and update connection credentials
3. Run the Python data cleaning script to preprocess the raw dataset
4. Load the cleaned data into PostgreSQL via SQLAlchemy
5. Execute the SQL scripts in `sql/` to reproduce the business analysis
6. Open the `.pbix` file in Power BI to explore the interactive dashboard

---

## 👩‍💻 Author

**Rutuja**
Data Analytics | Business Analyst | Aspiring Data Scientist
🔗 [GitHub](https://github.com/Rutuja9298)

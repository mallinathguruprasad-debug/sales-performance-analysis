# Sales Performance Analysis

## 📊 Project Overview

This project performs an Exploratory Data Analysis (EDA) on a sales dataset to understand sales performance, product performance, customer markets, deal sizes, order status, and time-based sales trends.

The analysis focuses on identifying meaningful patterns and generating business insights that can support sales and marketing decisions.

---

## 🎯 Objectives

The main objectives of this project are:

- Understand the structure and quality of the sales dataset.
- Clean and prepare the data for analysis.
- Analyze numerical and categorical variables.
- Identify sales trends across products, countries, months, quarters, and years.
- Analyze the relationship between price, quantity, and sales.
- Identify high-performing product lines and markets.
- Compare total sales with average transaction value.
- Identify potential outliers in sales.
- Generate actionable business insights.

---

## 🗂️ Dataset

The dataset contains **2,823 sales records and 25 columns**.

### Important Columns

| Column | Description |
|---|---|
| `ORDER_NUMBER` | Unique order identifier |
| `QUANTITY_ORDERED` | Number of products ordered |
| `PRICE_EACH` | Price of each product |
| `SALES` | Sales value of the order line |
| `ORDER_DATE` | Date of the order |
| `STATUS` | Order status |
| `QTR_ID` | Quarter of the order |
| `MONTH_ID` | Month of the order |
| `YEAR_ID` | Year of the order |
| `PRODUCT_LINE` | Product category |
| `MSRP` | Manufacturer's suggested retail price |
| `CUSTOMER_NAME` | Customer name |
| `CITY` | Customer city |
| `COUNTRY` | Customer country |
| `TERRITORY` | Sales territory |
| `DEAL_SIZE` | Deal size classification |

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## 🔍 Data Cleaning

The following data-cleaning steps were performed:

- Checked dataset dimensions and data types.
- Checked missing values.
- Checked duplicate records.
- Converted `ORDER_DATE` to datetime format.
- Investigated missing geographical and address information.
- Checked numerical variables for unusual values.
- Used the IQR method to identify potential sales outliers.
- Retained potential outliers because they may represent genuine high-value transactions.

---

## 📈 Exploratory Data Analysis

### Univariate Analysis

The following variables were analyzed individually:

- Sales
- Quantity Ordered
- Price Each
- MSRP
- Product Line
- Deal Size
- Order Status
- Country
- Territory
- City
- Year
- Quarter
- Month
- Order Line Number

Histograms, countplots, bar charts, and descriptive statistics were used to understand the distributions.

### Bivariate Analysis

Relationships were analyzed between:

- Product Line vs Sales
- Country vs Sales
- Deal Size vs Sales
- Order Status vs Sales
- Year vs Sales
- Quarter vs Sales
- Month vs Sales
- Quantity Ordered vs Sales
- Price Each vs Sales
- MSRP vs Sales
- Product Line vs Deal Size

A correlation heatmap was also created to analyze relationships between numerical variables.

---

# 🔑 Key Findings

### 1. Product Line Performance

**Classic Cars** is the strongest-performing product line.

- Total sales: approximately **3.92 million**
- Average sales per transaction: approximately **4,053.38**

Classic Cars performs strongly in both total revenue and average transaction value.

---

### 2. Deal Size Performance

**Medium deals** generate the highest total sales revenue.

| Deal Size | Records |
|---|---:|
| Medium | 1,384 |
| Small | 1,282 |
| Large | 157 |

However, **Large deals have the highest average transaction value**, at approximately **8,293.75**.

This shows the difference between transaction volume and transaction value.

---

### 3. Country Performance

The **USA** generates the highest total sales revenue, at approximately **3.63 million**.

Other major markets include:

- Spain
- France
- Australia
- UK
- Italy

Denmark has the highest average sales among the top countries, at approximately **3,899**.

---

### 4. Time-Based Performance

**2004** recorded the highest total sales revenue:

- 2003: approximately **3.52 million**
- 2004: approximately **4.72 million**
- 2005: approximately **1.79 million**

Quarter 4 has the highest recorded quarterly sales revenue at approximately **3.87 million**.

**November** is the strongest month, with approximately **2.12 million** in sales.

---

### 5. Order Status

The majority of records are classified as **Shipped**.

- Shipped records: **2,617**
- Shipped sales: approximately **9.29 million**

Other statuses such as Cancelled, On Hold, Resolved, In Process, and Disputed represent a much smaller proportion of the dataset.

---

### 6. Correlation Analysis

The strongest relationships with `SALES` were:

| Variable | Correlation with Sales |
|---|---:|
| `PRICE_EACH` | **0.66** |
| `MSRP` | **0.64** |
| `QUANTITY_ORDERED` | **0.55** |

These indicate positive relationships with sales.

The results suggest that price-related variables and quantity ordered are associated with higher sales values.

> Correlation indicates association and does not prove causation.

---

# 💡 Business Insights & Recommendations

### 1. Focus on High-Performing Products

Classic Cars generates the highest total and average sales. The company should continue investing in this product line through targeted marketing and inventory planning.

### 2. Increase High-Value Transactions

Large deals have the highest average transaction value. Sales teams can target suitable customers with premium products, bundles, and personalized offers.

### 3. Strengthen the USA Market

The USA is the largest revenue-generating market. The company should maintain strong customer relationships while exploring growth opportunities in other markets.

### 4. Prepare for Peak Sales Periods

Q4 and November show strong sales performance. Inventory, staffing, and marketing campaigns should be planned ahead of these peak periods.

### 5. Improve Low-Performing Periods

June has the lowest monthly sales revenue. Targeted promotions and marketing campaigns could be considered during weaker sales periods.

### 6. Use Pricing Strategically

Price-related variables show strong positive associations with sales. Pricing analysis can support better product pricing and promotional decisions.

### 7. Monitor Order Status

Cancelled, On Hold, Disputed, and In Process orders should be monitored to identify operational issues and reduce potential revenue loss.

---

# 📁 Project Structure

```text
Sales_Performance_Analysis/
│
├── data/
│   └── sales_data_sample.csv
│
├── notebooks/
│   └── sales_eda.ipynb
│
├── README.md
│
└── .gitignore
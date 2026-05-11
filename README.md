# 🛒 E-Commerce Data Analysis — EDA using NumPy & Pandas

A structured exploratory data analysis of an e-commerce dataset, covering data cleaning with advanced NumPy imputation techniques, revenue summaries, category-wise sales, country-wise orders, customer insights, and time-based sales trends.

---

## 📌 Project Overview

This project demonstrates a complete EDA workflow on an e-commerce dataset — from raw dirty data to clean, actionable business insights. It highlights advanced data cleaning using **NumPy random sampling** to impute missing values based on column distributions, followed by multi-dimensional analysis across categories, countries, customers, and time periods.

---

## 📂 Dataset

- **File used:** `ecommerce.csv`
- **Key columns:** `Order_ID`, `Customer_ID`, `Order_Date`, `Product`, `Category`, `Price`, `Quantity`, `Country`
- **Derived column:** `Total` = `Price × Quantity`

---

## 🧹 Data Cleaning (Advanced)

| Column | Issue | Solution |
|---|---|---|
| `Order_ID` | Null values | Filled using row index + 1 |
| `Customer_ID` | Null values | Filled using `np.random.choice` from top 4 most frequent IDs |
| `Quantity` | Null values | Imputed using `np.random.uniform` based on distribution analysis |
| `Price` | Null values | Imputed using `np.random.uniform` (0–10,000 range) |
| `Country` | Null values | Filled using `np.random.choice` from top 3 most frequent countries |
| `Order_Date` | Object type | Converted to datetime using `pd.to_datetime` |

> Distribution of `Quantity` and `Price` was checked with histograms before choosing the imputation strategy.

---

## 🔍 Analysis Breakdown

### 📊 Data Summary
- Total number of orders
- Total number of customers
- Total revenue generated
- Average order value

### 🏷️ Category Analysis
- Revenue per product within each category
- Percentage sales share of each product within its category
- Grouped bar chart — category-wise product percent share

### 🌍 Country-wise Analysis
- Top 5 countries by number of orders
- Bar chart of order count per country

### 📅 Monthly Revenue Trend
- Line plot of total revenue over the entire date range

### 👤 Customer Insights
- Top 5 customers by total spending
- Bar chart of total spend per customer ID

### 💰 Price Distribution
- Histogram of product prices across ranges (0–10,000 in bins of 1,000)

### 📆 Time-based Analysis
- **Yearly average sales** — line plot
- **Quarterly average sales** — line plot
- Side-by-side comparison of both trends

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading, cleaning & aggregation |
| NumPy | Random imputation & numerical operations |
| Matplotlib | Bar charts & line plots |
| Seaborn | Histograms, bar plots & line plots |
| Google Colab | Development environment |

---

## 🚀 How to Run

### Option 1 — Open in Google Colab
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

*(Replace with your actual Colab notebook link)*

### Option 2 — Run Locally
```bash
git clone https://github.com/anshu1516/Ecommerce-EDA-Numpy-Pandas.git
cd Ecommerce-EDA-Numpy-Pandas

pip install pandas numpy matplotlib seaborn

jupyter notebook Exploratory_Data_Analysis__EDA__using_Numpy_and_Pandas.ipynb
```

> **Note:** Place `ecommerce.csv` in the same directory before running.

---

## 💡 Key Insights

- 🌏 **China, Indonesia, and Russia** are among the top countries by order volume
- 💸 A small group of customers contribute disproportionately to total revenue
- 📦 Price distribution is spread across a wide range — the platform sells both budget and premium products
- 📈 Quarterly and yearly trends reveal seasonality patterns in average sales

---

## 👤 Author

**Anshu** — [GitHub](https://github.com/anshu1516)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

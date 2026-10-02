# 🛒 E-Commerce Sales Analyzer

A **Python Pandas-based data analysis project** that analyzes e-commerce sales data to understand sales performance, revenue, product trends, customer behavior, and order patterns.

## 📌 Project Overview

The **E-Commerce Sales Analyzer** uses **Python and Pandas** to clean, process, analyze, and extract useful insights from an e-commerce sales dataset.

The project covers important data-analysis operations such as:

* Loading CSV data
* Exploring the dataset
* Checking data types and missing values
* Handling missing values
* Removing duplicate records
* Converting date columns
* Calculating revenue
* Analyzing sales performance
* Finding average ratings
* Identifying trends and patterns

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Jupyter Notebook / VS Code**
* **CSV Dataset**

## 📂 Project Structure

```text
E-Commerce-Sales-Analyzer/
│
├── ecommerce_sales.csv
├── ecommerce_sales_analyzer.py
├── E-Commerce-Sales-Analyzer.ipynb
├── README.md
└── requirements.txt
```

## 📊 Dataset

The dataset contains e-commerce order information such as:

| Column       | Description                    |
| ------------ | ------------------------------ |
| `Order_ID`   | Unique ID of the order         |
| `Order_Date` | Date when the order was placed |
| `Product`    | Product name                   |
| `Category`   | Product category               |
| `Quantity`   | Number of products ordered     |
| `Price`      | Price of the product           |
| `Rating`     | Customer rating                |
| `Customer`   | Customer information           |

> **Note:** Column names may vary depending on the dataset used.

## 🔍 Data Analysis Process

### 1. Import Pandas

```python
import pandas as pd
```

### 2. Load the Dataset

```python
df = pd.read_csv("ecommerce_sales.csv")
```

### 3. Explore the Data

```python
print(df.head())
print(df.shape)
print(df.columns)
print(df.dtypes)
```

### 4. Check Missing Values

```python
print(df.isnull().sum())
```

### 5. Calculate Average Rating

```python
average_rating = df["Rating"].mean()
print(average_rating)
```

### 6. Fill Missing Ratings

```python
df["Rating"] = df["Rating"].fillna(df["Rating"].mean())
```

### 7. Remove Duplicate Records

```python
df = df.drop_duplicates()
```

### 8. Convert Order Date

```python
df["Order_Date"] = pd.to_datetime(df["Order_Date"])
```

### 9. Create Revenue Column

```python
df["Revenue"] = df["Quantity"] * df["Price"]
```

## 📈 Key Analysis

The project can be extended to answer questions such as:

* What is the total revenue?
* Which product generated the highest revenue?
* Which category has the highest sales?
* What is the average product rating?
* Which month had the highest sales?
* Which products are ordered most frequently?
* What is the average order value?
* Which customers generated the highest revenue?

### Example

```python
total_revenue = df["Revenue"].sum()
print("Total Revenue:", total_revenue)
```

Find the product with the highest revenue:

```python
product_sales = df.groupby("Product")["Revenue"].sum()

print(product_sales.sort_values(ascending=False))
```

## 🎯 Project Objectives

1. Understand and explore e-commerce sales data.
2. Clean missing and duplicate data.
3. Perform data transformation using Pandas.
4. Calculate important sales metrics.
5. Identify useful business insights.
6. Practice real-world data analysis techniques.

## 💡 Skills Demonstrated

* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis (EDA)
* Data Transformation
* Pandas DataFrames
* GroupBy Operations
* Date & Time Analysis
* Missing Value Handling
* Duplicate Detection
* Basic Business Analytics

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/E-Commerce-Sales-Analyzer.git
```

### Step 2: Open the Project

```bash
cd E-Commerce-Sales-Analyzer
```

### Step 3: Install Dependencies

```bash
pip install pandas numpy
```

Or:

```bash
pip install -r requirements.txt
```

### Step 4: Run the Project

If using Python:

```bash
python ecommerce_sales_analyzer.py
```

If using Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
E-Commerce-Sales-Analyzer.ipynb
```

## 📋 Sample Requirements

Create a `requirements.txt` file containing:

```text
pandas
numpy
jupyter
```

## 🔮 Future Improvements

* Add data visualizations using **Matplotlib**
* Create interactive dashboards
* Add monthly and yearly sales analysis
* Perform customer segmentation
* Add sales forecasting
* Build a Power BI dashboard
* Automate the analysis pipeline

## 👨‍💻 Author

**Rakesh Vishwanath**

B.Tech – Computer Science Engineering

## ⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

**Built with Python 🐍 and Pandas 🐼**
